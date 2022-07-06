# Una breve introducción a la teoría de tipos

Como muchos de vosotros sabréis, una gran parte de las matemáticas se encuentran construidas sobre los poderosos pilares que son los **axiomas de Zermelo-Fraenkel** y, por ende, sobre la **teoría de conjuntos**. Sin embargo, esta teoría puede llegar a ser *poco intuitiva* a la par que *compleja para las computadoras*; por ende, hoy exploraremos la que es, probablemente, su alternativa más sólida y confiable: La **teoría de tipos**.

Pero, antes de nada, comencemos por el principio... Para demostrar un afirmación *(sea, por ejemplo, que* $2 + 3 = 5$*)* requerimos de **teoremas**, y para demostrar estos otros teoremas *(los cuales, a su vez, son afirmaciones)* requerimos de más teoremas; siguiendo este camino hasta que llegamos a los **axiomas**, aquellas afirmaciones que asumimos que son verdaderas sin prueba alguna de ello.

Con los **axiomas de Zermelo-Fraenkel**, obtenemos una fuerte y confiable teoría, con el ligero problema de que tenemos que construir todo sobre la lógica, siendo nuestra teoría un superconjunto de esta. Sin embargo, en la **teoría de tipos**, la lógica y las matemáticas van a la par, algo que explicaremos más adelante en este mismo artículo.

Pero... ¿En qué consiste la teoría de tipos? Aquí, cada objeto u elemento posee un tipo que engloba a un conjunto de elementos similares, algo parecido a como funcionan la mayoría de lenguajes de programación, lo que denotaremos del siguiente modo:
$$
  a: A
  b: B
$$
Aquí, expresamos que el elemento $a$ tiene $A$ como tipo, y el elemento $b$ tiene $B$ como tipo.

Podemos además, construir tipos; por ejemplo, construyamos el tipo de dato **booleano** (al que denotaremos como $\beta$), el cuál puede ser o bien *verdadero* o bien *falso*:
$$
  V: \beta
  F: \beta
$$

Para este tipo, hemos requerido de solamente dos constructores, pero si quisiéramos construir un tipo de dato más complejo como lo podrían ser los **números naturales**, no sería eficiente tener infinitos constructores, uno para cada uno, sino que podríamos tener en este caso un número base *(el* $1$*, por ejemplo)* y una función que nos otorgue el sucesor inmediato de un natural *(ese mismo* $n$ *incrementado en una unidad)*, construyendo así cada número:
$$
  1: \mathbb{N}
  ^{+}: \mathbb{N} \rightarrow \mathbb{N}
$$

Además, podemos **combinar tipos de datos** para crear nuevos; por ejemplo, denotaremos $A\rightarrow B$ como el tipo de dato de una función que toma un elemento de $A$ como argumento y retorna uno de $B$, representaremos además $A\times B$ como el tipo de dato de una dupla $(a, b)$ donde $a$ tiene como tipo $A$ y $b$ tiene como tipo $B$.

La ventaja que os mencioné anteriormente acerca de la teoría de tipos consiste en que los tipos pueden ser pensados a su vez como **proposiciones**, donde cada elemento sería una **demostración** para estas. Además, podemos pensar de $A\rightarrow B$ como $A$ implica $B$ o $A\times B$ como $A$ y $B$.

Así, la tarea de ver si una proposición dada es verdadera o falsa consiste en hallar su tipo correspondiente y tratar de encontrar un elemento de este mismo tipo.

Si os ha interesado este tópico, os recomiendo [el vídeo del usuario “Dapper Mink”](https://youtu.be/QRrcwahx-3s) aún estando en inglés, él me ha inspirado para hacer esta entrada del blog y su charla es increíble.
