# Novedades del nuevo Python 3.11

Como muchos de vosotros ya sabréis, **Python 3.11** saldrá a la luz dentro de unos pocos días y, por este motivo, me ha parecido oportuno hacer una recapitulación sobre las novedades que tendrá esta nueva versión del aclamado lenguaje de programación.

Comenzando por las mejoras más destacables, **Python 3.11** será **entre un 10% y un 60% más veloz** en comparación a su versión anterior, además de que esta nueva entrega contará con una funcionalidad que hará que la depuración de proyectos sea mucho más rápida y efectiva; me refiero a la *localización exacta de los fallos cuando ocurra un error en tu programa*, funcionalidad que se llevará a cabo **subrayando la expresión exacta** donde se originó el susodicho error, como se ilustra en el siguiente ejemplo:
```python
Traceback (most recent call last):
  File "distance.py", line 11, in <module>
    print(manhattan_distance(p1, p2))
          ^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "distance.py", line 6, in manhattan_distance
    return abs(point_1.x - point_2.x) + abs(point_1.y - point_2.y)
                           ^^^^^^^^^
AttributeError: 'NoneType' object has no attribute 'x'
```

Además, y continuando con este mismo tema, Python ha agregado una nueva clase cuya funcionalidad es, simplemente, *agrupar varias excepciones con poca o nula semejanza entre las mismas*; estas pueden ser atrapadas en bloques `try/except` utilizando la nueva sintaxis except*, la cual *(como ya hemos mencionado)* atrapa no solo una excepción sino un grupo entero. Mencionar además que, ahora, las excepciones poseen un nuevo método integrado llamado `add_note`, el cual toma una cadena de texto como argumento y resulta en información añadida al error en cuestión, algo que en combinación con bloques `try/except` puede resultar en una buena utilidad para el lenguaje.

Esta nueva edición de Python ha traído, sobre todo, novedades en el tipado estático del lenguaje, añadiendo clases como `TypeVar` para la *creación de tipos genéricos*, marcadores para *indicar propiedades requeridas o no requeridas* en diccionarios, el tipo `Self` para indicar que *se retorna o requiere un elemento de la misma clase* a la hora de crear métodos para la misma y el tipo de dato `LiteralString`, que implica el uso de una cadena de texto literal *(como lo podrían ser ‘foo’ o ‘bar’)*, tipo de dato que podría ser muy útil a la hora de *realizar consultas a bases de datos*.

Además, entre otros cambios del lenguaje se ha añadido el nuevo módulo `tomllib`, utilizado para *parsear código TOML*; mencionar también la mejora de otros módulos del lenguaje como `asyncio`, `datetime`, `fractions` o `functools` entre muchos otros.

Sin duda alguna, **Python 3.11** se ve genial y supondrá un gran cambio al lenguaje, aunque quizás no tan gigante como lo fue **Python 3.10**, al menos desde mi punto de vista. De todos modos siempre podéis leer [el documento con todas las nuevas mejoras](https://docs.python.org/es/3.11/whatsnew/3.11.html) para así juzgar bajo vuestro propio criterio.
