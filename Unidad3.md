## Índice

- [Resumen teórico](#resumen-teórico)
- [Ejercicios resueltos](#ejercicios-resueltos)
- [Ejercicio aplicado en un caso real](#ejercicio-aplicado-en-un-caso-real)
- [Reflexión personal](#reflexión-personal)
- [Actividades](#actividades)

---

## Resumen teórico

### Definición de Grafo

Se describe formalmente como una tripleta \(G = (V, E, \phi)\), donde \(V\) es un conjunto de vértices, \(E\) de aristas y \(\phi\) es la función de incidencia.

### Terminología Clave

- **Orden:** Número total de vértices.
- **Tamaño:** Número total de aristas.
- **Grado (Valencia):** Número de aristas que llegan a un nodo.

### Tipos de Recorridos

- **Euler:** Recorre todas las aristas exactamente una vez. Un grafo conexo tiene un circuito de Euler si todos sus vértices son de grado par.
- **Hamilton:** Visita cada vértice exactamente una vez. Su resolución es un problema NP-completo.

### Algoritmos de Optimización

- **Fleury:** Método para construir caminos eulerianos evitando cruzar "puentes" a menos que sea necesario.
- **Dijkstra:** Algoritmo para hallar la ruta más corta en grafos con aristas de peso no negativo mediante etiquetas temporales y permanentes.

### Representación Matricial

Las computadoras procesan grafos mediante la **Matriz de Adyacencia** (útil para calcular caminos de longitud \(k\)) y la **Matriz de Incidencia** (ideal para multigrafos).

### Teoría de Árboles

Un árbol es un grafo conexo acíclico. Se estudian árboles binarios de búsqueda (BST) y sus recorridos: inorden, preorden y posorden.

---

## Ejercicios resueltos

### Ejercicio 1: Isomorfismo de Grafos

**Problema:** Determinar si los grafos \(G_1\) y \(G_2\) son isomorfos.

**Procedimiento:** Se comparan los grados de los vértices. En \(G_1\), el vértice \(c\) tiene grado 2, pero en el mapeo propuesto a \(G_2\), el vértice \(v_1\) tiene grado 3.

**Resultado:** No son isomorfos bajo la función \(f\), ya que no conservan la estructura de grados ni las aristas correspondientes.

---

### Ejercicio 2: Demostración de la Fórmula de Euler

**Problema:** Demostrar \(V - A + C = 2\) mediante inducción sobre las aristas.

**Procedimiento:**

- **Caso base:** Un vértice, 0 aristas, 1 cara (\(1 - 0 + 1 = 2\)).
- **Paso inductivo:** Al añadir una arista, o bien se añade un vértice (V y A aumentan en 1, manteniendo la igualdad), o bien se cierra un ciclo (A y C aumentan en 1, manteniendo la igualdad).

**Resultado:** La fórmula es válida para cualquier grafo plano conectado.

---

### Ejercicio 3: Coloreado de un Cubo

**Problema:** ¿Cuál es el número cromático de un cubo?

**Procedimiento:** Un cubo solo tiene ciclos de longitud par (caras cuadradas), lo que lo define como un grafo bipartito.

**Resultado:** El número mínimo de colores es **2**.

---

### Ejercicio 4: Triángulo Monocromático en \(K_6\)

**Problema:** Demostrar que en un grafo completo de 6 vértices coloreado con dos colores siempre hay un triángulo monocromático.

**Procedimiento:** Aplicando el **Principio del Palomar**, un vértice \(v\) tiene 5 aristas; al menos 3 deben ser del mismo color (ej. rojo). Si alguna arista entre esos 3 vecinos es roja, se forma el triángulo; si ninguna lo es, los 3 vecinos forman un triángulo del otro color.

**Resultado:** La existencia de un triángulo monocromático está garantizada.

---

### Ejercicio 5: Cobertura de Vértices y Emparejamiento

**Problema:** Relación entre el tamaño de la cobertura mínima y el emparejamiento máximo.

**Procedimiento:** Se utiliza la desigualdad \(\nu(G) \le \tau(G) \le 2\nu(G)\). En grafos bipartitos, ambos valores coinciden.

**Resultado:** En grafos generales, la cobertura puede ser hasta el doble del emparejamiento.

---

## Ejercicio aplicado en un caso real

### Planteamiento del problema

Se modeló un grupo de 8 amigos donde las aristas representan los años de amistad (peso).

### Análisis con lógica y grafos

- **Vértices:** Ana, Bruno, Carla, Diego, Elena, Felipe, Gaby, Hugo.
- **Conectividad:** El grafo es conectado; no hay integrantes aislados.
- **Caminos Críticos:** Los nodos C, D y F son críticos para la conexión del grupo.

### Resultado del análisis

Mediante el algoritmo de Dijkstra, se determinó que el camino más corto (en años de amistad acumulados) entre Ana y Hugo es \(A \rightarrow C \rightarrow E \rightarrow F \rightarrow H\), con un total de 15 años.

---

## Reflexión personal

### ¿Qué fue lo más difícil de entender?

Diferenciar los recorridos de Euler (aristas) y Hamilton (vértices), y comprender la complejidad NP-completa de estos últimos.

### ¿Qué temas comprendí mejor?

La representación matricial de grafos y cómo el álgebra lineal (potencias de matrices) facilita el conteo de caminos en sistemas computacionales.

### ¿Cómo puedo aplicar la teoría de grafos en mi carrera?

La teoría de grafos permite optimizar infraestructuras de red, diseñar algoritmos de enrutamiento más eficientes (como Dijkstra en GPS) y gestionar bases de datos relacionales.

---

## Actividades


- [Actividades Practico Experimentales](APEU3.md)
- [Actividades Autonomas](AAU3.md)
- [Actividad Contacto Docente](ACDU3.md)
- [Evaluacion Sumativa](ESU3.md)
- 
[Regresar](Portafolio.md)
