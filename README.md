Ejemplos de orientación a objetos con C++
=========================================

# Uso de clases abstractas

[Fichero principal EjemploClasesAbstractas.cpp
](https://github.com/javism/EjemplosCpp/blob/master/src/EjemploClasesAbstractas.cpp "")

[Implementación clases
](https://github.com/javism/EjemplosCpp/tree/master/src/ClassesAbstractas "")

Este ejemplo demuestra cómo utilizar clases abstractas en C++. El objetivo del ejemplo es mostrar cómo una clase madre abstracta define una interfaz de programación común para las clases o programas que la utilicen.

En este ejemplo la clase madre Poligono define la funcion area(), y obliga a las clases hijas a implementar esta función. En el ejemplo las clases Cuadrado y Rectángulo son clases hijas que implementan la función area().

![Diagrama de clases del ejemplo](doc/inherit_graph_0.png "Diagrama de clases del ejemplo")

El código del programa principal tiene una función que recibe un objeto de la clase madre (Polígono), y llama a la función area().

void imprime_area(Poligono* pol)

En el código se declara primero un objeto rectángulo y otro cuadrado y se llama a imprime_area() pasándole cada vez un objeto. 

Esto es posible porque en OO una variable del tipo clase madre puede contener objetos del tipo de las clases hijas.

En la segunda parte del código se utiliza una clase que usa la clase Poligono de forma genérica. Así, podemos configurar la clase UsadoraPoligono fijando el objeto de tipo polígono en un rectángulo o en un cuadrado. La clase UsadoraPoligono se desacopla de qué subclase recibe, simplemente llama a area() que es la interfaz que proporciona la clase superior.
