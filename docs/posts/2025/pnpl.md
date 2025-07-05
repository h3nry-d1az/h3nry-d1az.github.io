# PNPL: An Esoteric Language Based on Prime Numbers

<header>May 16, 2025</header>
<br>
<hr>

I have finally made a programming language, but it is not conventional by any means. The internet is full of Python and Rust clones which, although they try to bring some new twists to the table, in practice turn out to be a worse choice than those who they copy; and it is such a shame because it makes one think that everything has already been invented and there is no room for innovation at all, despite the tremendous work their creators have devoted.

However, there is still a very geek niche named *esoteric languages* -- its name references their obscurity and weirdness -- where almost anything can be found. Do you need a minimal, Turing-complete language with as few as 4 instructions? [Here it is what you were looking for](https://esolangs.org/wiki/P%E2%80%B2%E2%80%B2). You have been trying to find a C-like language that uses Arnold Schwarzenegger's best quotes as keywords? [They have got you suited](https://esolangs.org/wiki/ArnoldC). Overall, one will not find as much creativity as in the [Esolangs wiki](https://esolangs.org/wiki/Main_Page), where the main goal is just to achieve Turing-completeness, and everything else are unnecessary abstractions.

That is exactly the reason why today I am announcing PNPL, an esoteric language that revolves around prime numbers and the uniqueness of their products.

# A story from three years ago

Actually, I might have just told a white lie, because I did not come up with its core idea a few days ago, but rather the concept of a language based on the fundamental theorem of arithmetic (FTA from now on) has been coming to my mind at least since 2022. This was originally the final project me and my friends Adam and Alessandro made for the ESTALMAT program, and was named pirho (\\(\\Pi_\\rho\\)), for *product (of primes)*.

In \\(\\Pi_\\rho\\), programs are made up of a list of numbers separated by spaces, where each one represents a different instruction. Now, each instruction is composed of an opcode -- denoted by a prime number --, and a series of arguments, all multiplied together so that they can be recovered by the FTA. For example, here is a valid \\(\\Pi_\\rho\\) program: \\[959\\:11\\:89\\:101\\:10349\\quad\\implies\\quad 7\\cdot 137\\: 11 \\: 89\\: 101\\: 79\\cdot 131 \\]

The first two numbers store an input character from the user in memory (analog to C's `getch`), and prints it if it differs from 0x00, otherwise it repeats the process from the beginning.

In total, \\(\\Pi_\\rho\\) had a total of 30 different instructions plus 6 special registers in order to make the programming experience less harsh, a decission that does not make much sense when put in perspective considering it was ultimately an esoteric language. \\(\\Pi_\\rho\\)'s syntax was inconvenient as well, because, for example, the operation \\(7\\cdot 22\\) would be interpreted as \\(2\cdot 77\\) by the interpreter, as a result of the commutativity of integer multiplication.

However, the original paper describing \\(\\Pi_\\rho\\) is not available on the internet, and neither is the interpreter I made.

# A better reimagination

Thus, PNPL is meant to be a recreation of the concept above, but aiming at the following:

* A consistent syntax, with no *misinterpreted operations*.
* Every possible program must be a single number, not a list of integers.

And it was indeed possible to achieve! I will not really repeat myself because I have already described the functioning twice (in both the [GitHub repository](https://github.com/h3nry-d1az/pnpl) and [Esolangs wiki](https://esolangs.org/wiki/PNPL)), but I will summarize it as a [Goedel numbering](https://plato.stanford.edu/entries/goedel-incompleteness/sup1.html) frontend for a Brainfuck interpreter, this last peculiarity grants Turing-completeness to the language.

# Final thoughts
Overall, it has been quite a fun project to make and the culmination of an intrusive thought that has spanned for a few years.