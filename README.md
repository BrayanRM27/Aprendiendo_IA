# Implementación de BFS y DFS en Python

## Descripción

En este proyecto se realizó la implementación y comparación de dos algoritmos clásicos de recorrido de grafos: **Breadth-First Search (BFS)** y **Depth-First Search (DFS)**.

Antes de realizar la implementación del código, primero investigué cómo funcionan ambos algoritmos. Para ello revisé diferentes recursos y videos explicativos donde se mostraba el funcionamiento de BFS y DFS, especialmente cómo realizan los recorridos sobre un grafo y qué estructuras de datos utilizan internamente.

Una vez comprendido cómo funcionan los recorridos y la lógica de cada algoritmo, procedí a implementar ambos en Python utilizando el mismo grafo para poder comparar su comportamiento y el uso de memoria durante la ejecución.

El código fue desarrollado y probado utilizando **Google Colab**, lo que permitió ejecutar el programa directamente desde el navegador.

## Estructura del grafo

El grafo utilizado en el ejercicio tiene la siguiente estructura:

```
      A
     / \
    B   C
   / \   \
  D   E   F
     /
    G
```

Las conexiones entre los nodos se representan en Python mediante un **diccionario**, donde cada nodo contiene una lista con sus vecinos.

## Algoritmos implementados

### BFS (Breadth-First Search)

El algoritmo **BFS** recorre el grafo **por niveles**, visitando primero los nodos más cercanos al nodo inicial.

Para su implementación se utiliza una **cola (queue)** que almacena los nodos pendientes por visitar.

Durante la ejecución del programa se muestra:

* El nodo que se está visitando.
* El estado de la cola de nodos pendientes.
* El recorrido final del algoritmo.
* La memoria máxima utilizada, medida como la cantidad máxima de nodos almacenados en la cola.

### DFS (Depth-First Search)

El algoritmo **DFS** recorre el grafo explorando una rama completa antes de retroceder y continuar con otra.

En este proyecto se implementa utilizando **recursión**, por lo que el control del recorrido se realiza mediante la pila de llamadas del programa.

Durante la ejecución el programa muestra:

* Cuándo el algoritmo entra a un nodo.
* Cuándo retrocede (backtracking).
* El recorrido final obtenido.
* La profundidad máxima alcanzada, que representa la memoria utilizada por la pila de llamadas.

## Comparación de resultados

Al ejecutar ambos algoritmos sobre el mismo grafo se obtienen diferentes recorridos:

**BFS:** A → B → C → D → E → F → G
**DFS:** A → B → D → E → G → C → F

En cuanto al uso de memoria:

* **BFS** depende principalmente del **ancho del grafo**, es decir, la cantidad de nodos que existen en un mismo nivel.
* **DFS** depende de la **profundidad de las ramas**, ya que solo mantiene en memoria el camino actual que está explorando.

Aunque en este ejemplo el consumo de memoria es similar, en grafos más grandes **BFS suele requerir más memoria que DFS**, porque debe almacenar todos los nodos de un mismo nivel en la cola.

## Autor

Brayan David Riasco
