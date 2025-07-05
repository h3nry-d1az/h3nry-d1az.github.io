# Type Theory, Lean, and "Perfect" Mathematics

<header>Sep 30, 2024</header>
<br>
<hr>

One may think of mathematics as a colossal, millennia-old Lego building; maybe not one with plentiful colors, or numerous figurines decorating the scenery, and possibly even lacking any sort of interesting shape, but surely one in which each building block corresponds to a different result or fact -- for example, you could think of Euclid's division lemma and Stokes' theorem as yet another blocks that support the weight of many others.

This analogy turns out to be more helpful than it might seem at first glance, since it exposes an intriguing detail, namely, that such a construction must have some sort of foundation, some bedrock upon which the rest edifies; in logic, this translates to the fact that _from nothing, nothing comes!_

These primitive truths are called **axioms**, and are often propositions considered so obvious that they demand no proof whatsoever, hence, chosen not to be demonstrated but rather assumed as the starting point of the mathematical journey. Currently, our *de facto* set of axioms is named ZF(C), which stands for Zermelo-Fraenkel (the name of its two creators) with possibly the [axiom of choice](https://plato.stanford.edu/entries/axiom-choice/), which I will completely neglect during the entirety of this article (sorry AC fans, and sorry to the rest of you all for the pun).

What may surprise those unseasoned with low-level math, is that ZF(C) only defines **set theory**, and the rest, the entirety of the vast ecosystem of mathematics, *is defined as sets and sets of sets*. Furthermore, and to the utter wonder of anyone reading this, those sets all boil down to the **empty set** (\\(\varnothing\\)), which blows my mind.

# The axioms of ZF(C)
This is not really related to the topic of today -- and you can definitely skip it if you wish --, but just for the sake of completeness, let's talk briefly about the aforementioned axiomatic system, namely ZF -- again, I'll omit the axiom of choice --. It actually consists of **infinite** axioms, but don't worry, this is because it makes use of a little trick called *axiomatic schemes*, but let's not get ahead of ourselves and start from the beginning.

Paradoxically, ZF does not give any definition at all for the concept of *set*, but if you think about it twice, it really doesn't have to! If I tell you that all bulls have horns, and I tell you I've got a bull, you can properly conclude that my creature has indeed horns. You do not need the subjects to do the logic, logic itself is enough!

If you want an intuitive approximation of what a set is, though, just think about it as a box with (or even without) stuff, things there have no order, and you cannot have duplicates either (in contrast to real life). That's pretty much what a set is.

By the way, I will be writing down the statement in both plain English and formal logic, you are not required to know the latter, but I include it for the seasoned (and because I believe that, if you stare at them for long enough, you'll eventually learn some logic, c'mon, I believe in you). Anyway, here they go:

1. **Axiom of Extensionality**: Two sets are equal if they have the same elements: $$\forall X \forall Y \forall u (u \in X \iff u \in Y) \implies X = Y.$$ As I said, it does really seem trivial, but in the beginning there is nothing that ensures this proposition is true, so we just have to assume it.

2. **Axiom of the empty set**: There exists a set with nothing in it: $$\exists \varnothing \forall x (x \notin \varnothing).$$

2. **Axiom of Pairing**: For any two sets there exists another that contains only those two: $$\forall X \forall Y \exists \\{X,Y\\} \forall a (a \in \\{X,Y\\} \iff (a = X \lor a = Y)).$$

3. **Axiom of Comprehension**: If we have a set and a property, we can sieve the ones that meet it and put them in another set: $$\forall X \exists Y \forall u (u \in Y \iff (u \in X \land \phi(u)))$$

4. **Axiom of the Power Set**: For a given set, we can construct the set with all its subsets (sounds complicated but think about it twice): $$\forall X \exists \mathscr{P}X \forall u (u \in \mathscr P X \iff (\forall v (v \in u \implies v \in X))).$$

6. ...

I'm not going to list them all because it will be both boring and redundant since they are already [out there on the internet](https://mathworld.wolfram.com/Zermelo-FraenkelAxioms.html), and most importantly, because there is no need to provided this is not the main focus of this article.

# The story behind type theory
To understand why type theory even exists, we need to go back to the late 1800s and early 1900s when the attempt to find those "building blocks" of mathematics was at its peak. By then, a mathematician named Gottlob Frege proposed his own theory, which rapidly became very popular, until another mathematician, with name Bertrand Russell, found a flaw in Frege's axioms, the infamous **Russell's paradox**.

One of Frege's assumptions was that, given any (formal) statement, there existed a set containing all the sets that met it, so Russell said -- and here I paraphrase -- : "Oh yeah? So what about the property: '\\(x \notin x\\)' (\\(x\\) is not in \\(x\\))?" Which completely obliterated Frege's work. Let's think about why:

For the rest of the sets, there should be no problem, either they satisfy the property or they don't, but it shouldn't be a big deal. For the big, container set, however, we have two options:

1. The big set contains itself, and thus by our assumption the big set is not included in the big set.

2. The big set doesn't contain itself, and thus by our assumption the big set is included in itself.

One can see then that the former case leads to the latter, and the latter to the former in an infinite loop that is nothing but a <span style="font-size: 150%;">HUGE</span> contradiction. This clearly had to be fixed, so mathematicians back in the day began working on the issue.

The year is 1908, and two landmark papers are published. First, Zermelo's famous proposal, but Russell had his own idea two, what nowadays is known as **type theory**, and now, in the XXI century is achieving its prime popularity.

# Type theory as an alternative

If you have ever coded in a statically typed language, you sort of know what this business is all about. We have elements, namely \\(a, b, x, y, \ldots\\), &nbsp;-- which correspond to variables -- that can belong to a collection named **type**. We denote this ownership by $$x: \mathtt{type},$$ just like you would in Rust or TypeScript. Note that functions are still a thing, so for example, $$f: \mathtt{t}_1 \rightarrow \mathtt{t}_2$$ is an object that takes an input from a type \\(\mathtt{t}_1\\) and returns another from a type \\(\mathtt{t}_2\\). Furthermore, \\(\mathtt{t}_1 \rightarrow \mathtt{t}_2\\) is a type as well, and so is \\(\mathtt{t}_1 \times \mathtt{t}_2\\), and so forth.

With all this, type theory becomes a very robust framework, and the magic comes when we stop thinking of types as *sets*, and start thinking of them as **propositions**. Then, a member of the type will be a **proof** of the proposition, and the compound types \\(\mathtt{t}_1 \rightarrow \mathtt{t}_2\\) and \\(\mathtt{t}_1 \times \mathtt{t}_2\\) represent implication and conjunction respectively.

It is because of this comfortable correspondence with logic that type theory has been brought out of the "building blocks" scenario to work on more profitable contexts, the most important of which are **proof assistants**.

# Introducing Lean

Proof assistants are a marvelous, time-saving invention, they are basically programming languages in which you write the proof of your theorem, and it spits out whether it's correct or not, using type theory for the duty.

It's like having a [very pedantic] little fella next to you all the time, that ensures -- with a mathematically proven reliability -- that you are making no mistakes.

They appeared quite a while ago, one of the most popular, [Coq](https://coq.inria.fr/) (yes, that's its name, I won't argue it's quite funny), was first released back in 1989, but it is mainly because of the apparition of [Lean](https://www.lean-lang.org/) that they are experiencing a renaissance.

The latter, at least for my inexperienced taste, is far more elegant than the former, here is an example from the [Natural Number Game](https://adam.math.hhu.de/#/g/leanprover-community/nng4) about the associativity of the natural numbers, in my opinion, the best online resource for learning this tool:

```lean
theorem mul_assoc (a b c : ℕ) : (a * b) * c = a * (b * c) := by
    induction c with k hₖ

    repeat rw [mul_zero]
    repeat rw [mul_zero]
    rfl

    rw [mul_succ, mul_succ, mul_add, hₖ]
    rfl
```

You do not need to fully understand the proof, but simply notice the built-in induction statement, the easy support for Unicode characters, and, if you use Visual Studio Code, the amazing error spotting it provides. It may seem a hard tool to master at first glance, and indeed it is not easy, but surely it is not a waste of time either.

# "Perfect" Mathematics
This begs the question: "Can we ensure our mathematics are flawless using proof assistants?" The answer is sadly no because of Gödel's incompleteness theorems, but what we **can** do is to prove that, provided our assumptions, our proofs are valid, and there's a devoted collective out there trying to accomplish this dream. The proofs already exist, we just need to formalize them!

To close off, I would like to mention a project that is being carried out by the Imperial College of London, and which I do genuinely like, which is to [formalize Fermat's Last Theorem](https://github.com/ImperialCollegeLondon/FLT) in Lean.