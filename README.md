# Grafos - Ejercicio 2
Implementar un algoritmo que dado un grafo dirigido, no ponderado, débilmente conexo, disperso y acíclico devuelva el orden topológico. 

Ante la posibilidad de varios órdenes topológicos, desarrollar la estrategia que se describe a continuación. Supongamos el siguiente grafo:

<img width="259" alt="image" src="https://user-images.githubusercontent.com/35345672/165163806-9f83b157-2bfc-4af8-ab97-f19e9612e5b3.png">

Existen tres órdenes, a saber: <1,2,3,4>, <1,4,2,3> y <1,2,4,3>. Nuestro algoritmo debe retornar el último. La estrategia consiste en las siguientes dos condiciones:
- Ante la posibilidad de dos o más órdenes, siempre retornar el que contenga más cantidad de nodos “consecutivos en el mismo nivel”. Con esto último queremos decir que tanto <1,2,4,3> como <1,4,2,3> mantienen a 2 y 4 consecutivos, mientras que <1,2,3,4> no. Decimos que 2 y 4 pertenecen la mismo nivel porque se encuentra a la misma cantidad de saltos desde el primer vértice en el orden.
- En caso de que existan varios órdenes luego de aplicar la condición anterior, elegir el que sitúe a los nodos consecutivos en orden ascendente. En el ejemplo, el orden final será <1,2,4,3>.

## Restricciones
El algoritmo debe ejecutarse en O(E + V log V) tiempo de ejecución.
## Formato de entrada
[Formato de entrada del curso](https://docs.google.com/document/d/1pTUQ24hYRUQG5yxSQfuNHY_93Uh1_-acbIH-8EsRUUg/edit#heading=h.2k687rmdaqoi)

## Formato de salida
La salida contendrá V líneas, donde cada línea en la posición i representa al vértice vi que se encuentra en la posición i del orden topológico.
