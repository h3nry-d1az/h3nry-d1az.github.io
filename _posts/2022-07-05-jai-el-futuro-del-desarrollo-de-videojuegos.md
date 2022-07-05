# Jai, el futuro del desarrollo de videojuegos

Los que alguna vez hayáis visitado mi [canal de YouTube](https://www.youtube.com/channel/UCHcgIehZE12tL777Rx-hHgA), probablemente sepáis que la sección más popular del canal *(y mi favorita, dicho sea de paso)* consiste en probar y experimentar con [lenguajes de programación peculiares y desconocidos](https://www.youtube.com/watch?v=AE4K8CC-quw&list=PLwG1fQu9A7F25XuFwgGbU4mJqDB6MbIgE). Para este lenguaje de programación *(Jai)* me hubiera gustado hacer un vídeo con este mismo formato, sin embargo, no he sido capaz porque el lenguaje **todavía no existe**.

Me explico, Jai es un lenguaje de programación orientado a la creación de videojuegos y creado por *Jonathan Blow*, el famoso desarrollador de juegos indie, a quien muchos conoceréis por obras maestras como **The Witness**. Posee una sintaxis un tanto similar a **C++** *(como veremos más adelante)* pero con muchas más funcionalidades. No obstante, a día de hoy el compilador para este lenguaje no ha sido lanzado al público, existiendo sólo [las conferencias que el desarrollador ha dado](https://www.youtube.com/playlist?list=PLmV5I2fxaiCKfxMBrNsU1kgKJXD3PkyxO), las betas que ha proporcionado a varios usuarios y las [retransmisiones que él ha hecho por Twitch](https://www.twitch.tv/naysayer88).

Sin embargo, no poseer un compilador oficial para el lenguaje no ha detenido a una gran multitud de usuarios de crear sus propias [librerías y programas](https://repo.progsbase.com/), además de varios [compiladores no oficiales](https://github.com/airways/jai) para el lenguaje basados en la sintaxis mostrada en las charlas y [extensiones](https://inductive.no/jai/#:~:text=Discussion%3A%20Iteration-,Jai%20Tools,-jai%20compiler%20%E2%80%93%20not) para los editores de código más populares de hoy en día.

Sin embargo, el lenguaje Jai no se reduce a un mero clon de C++ con unas pocas mejoras, sino que se logra diferenciar con bastante claridad gracias a metas que se propone el lenguaje como lo son:
- Un alto rendimiento.
- La satisfacción de programar
- Una gran simplicidad.
- Poca *“fricción”*.
- Estar diseñado para buenos programadores.

No obstante, pienso que esto queda mejor ilustrado mediante un pequeño snippet de código como el siguiente, en el que se muestra el sistema de compilación que el lenguaje tendrá incorporado:
```c++
build :: () {
    build_options.executable_name = "my_program";
    print("Building program '%'\n", build_options.executable_name);
    build_options.optimization_level = Optimization_Level.DEBUG;
    build_options.emit_line_directives = false;

    update_build_options();

    // Jai will automatically build any files included with the #load directive,
    // but other files can also be manually added.
    add_build_file("misc.jai");
    add_build_file("checks.jai");
}

#run build();
```

El problema que yo, personalmente encuentro con Jai es que, más allá de su calidad, está tomando demasiado tiempo en ser desarrollado, pues **fue anunciado en el ya lejano 2019** y lenguajes de programación como Zig (del que, por cierto, [tengo un vídeo en el canal](https://www.youtube.com/watch?v=3FqLnNdm7BA)) le están comiendo terreno y podrían hacer que el lanzamiento del lenguaje deje a la comunidad de desarrolladores de videojuegos indiferente.

Desde este blog, quisiera transmitir mi apoyo al desarrollador y a su lenguaje, pues me parece un proyecto muy innovador y creo que tendrá una gran **repercusión** y **trascendencia**.
