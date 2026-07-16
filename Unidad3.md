<!-- ============================================ -->
<!--            NAVEGACIÓN RÁPIDA (UNIDADES)       -->
<!-- ============================================ -->
## Navegación rápida (Clic en el emoji)

<div align="center">
  <table>
    <tr>
      <td align="center" style="padding:15px; width:200px;">
        <a href="Unidad1.md" style="display:block; text-decoration:none; color:inherit;">
          <span style="font-size:40px;">1️⃣</span>
          <h3 style="margin:8px 0 4px 0;">Unidad 1</h3>
          <p style="margin:0; color:#586069;">Lógica proposicional</p>
        </a>
      </td>
      <td align="center" style="padding:15px; width:200px;">
        <a href="Unidad2.md" style="display:block; text-decoration:none; color:inherit;">
          <span style="font-size:40px;">2️⃣</span>
          <h3 style="margin:8px 0 4px 0;">Unidad 2</h3>
          <p style="margin:0; color:#586069;">Actividades</p>
        </a>
      </td>
      <!-- Resaltamos la Unidad 3 (donde estamos actualmente) -->
      <td align="center" style="padding:15px; width:200px; background-color:#f6f8fa; border-radius:8px;">
        <a href="Unidad3.md" style="display:block; text-decoration:none; color:inherit;">
          <span style="font-size:40px;">3️⃣</span>
          <h3 style="margin:8px 0 4px 0; color:#0366d6;">Unidad 3</h3>
          <p style="margin:0; color:#586069;">Grafos y optimización</p>
        </a>
      </td>
    </tr>
  </table>
</div>

---

<!-- ============================================ -->
<!--            ENCABEZADO DE LA UNIDAD 3          -->
<!-- ============================================ -->
## 📂 Unidad 3: Teoría de Grafos y Algoritmos

> En esta unidad exploramos los fundamentos de la teoría de grafos, desde su definición formal hasta algoritmos de optimización como Dijkstra y análisis de isomorfismos.

---

<!-- ============================================ -->
<!--                  ÍNDICE MEJORADO              -->
<!-- ============================================ -->
## 📑 Índice

<table align="center" style="border-collapse: collapse; width: 80%;">
  <tr>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#resumen-teórico" style="text-decoration: none; font-weight: bold; color: #0366d6;">📘 Resumen teórico</a>
    </td>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#ejercicios-resueltos" style="text-decoration: none; font-weight: bold; color: #0366d6;">📝 Ejercicios resueltos</a>
    </td>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#ejercicio-aplicado" style="text-decoration: none; font-weight: bold; color: #0366d6;">🤖 Ejercicio aplicado</a>
    </td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#reflexión-personal" style="text-decoration: none; font-weight: bold; color: #0366d6;">💭 Reflexión personal</a>
    </td>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#actividades" style="text-decoration: none; font-weight: bold; color: #0366d6;">📌 Actividades</a>
    </td>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#regresar" style="text-decoration: none; font-weight: bold; color: #0366d6;">🔙 Regresar</a>
    </td>
  </tr>
</table>

---

<!-- ============================================ -->
<!--             SECCIÓN: RESUMEN TEÓRICO          -->
<!-- ============================================ -->
## 📘 Resumen teórico

### 🔹 Definición de Grafo
Se describe formalmente como una tripleta \(G = (V, E, φ)\), donde \(V\) es un conjunto de vértices, \(E\) un conjunto de aristas y \(φ\) es la **función de incidencia** que asocia cada arista con un par de vértices.

### 🔹 Terminología Clave
- **Orden:** Número total de vértices.
- **Tamaño:** Número total de aristas.
- **Grado (Valencia):** Número de aristas que llegan a un nodo.

### 🔹 Tipos de Recorridos
- **Euler:** Recorre todas las aristas exactamente una vez. Un grafo conexo tiene un circuito de Euler si todos sus vértices son de grado par.
- **Hamilton:** Visita cada vértice exactamente una vez. Su resolución es un problema NP-completo.

### 🔹 Algoritmos de Optimización
- **Fleury:** Método para construir caminos eulerianos evitando cruzar "puentes" a menos que sea necesario.
- **Dijkstra:** Algoritmo para hallar la ruta más corta en grafos con aristas de peso no negativo mediante etiquetas temporales y permanentes.

### 🔹 Representación Matricial
Las computadoras procesan grafos mediante la **Matriz de Adyacencia** (útil para calcular caminos de longitud \(k\)) y la **Matriz de Incidencia** (ideal para multigrafos).

### 🔹 Teoría de Árboles
Un árbol es un grafo conexo acíclico. Se estudian árboles binarios de búsqueda (BST) y sus recorridos: inorden, preorden y posorden.

---

<!-- ============================================ -->
<!--           SECCIÓN: EJERCICIOS RESUELTOS      -->
<!-- ============================================ -->
## 📝 Ejercicios resueltos

---

### 🧩 Ejercicio 1: Análisis de Isomorfismo entre Grafos

**Planteamiento:** Dados dos grafos \(G_1\) y \(G_2\), determinar si la función \(f: G_1 \to G_2\) que mapea \(\{a,b,c,d,e,f,g\}\) a \(\{v_4, v_5, v_1, v_6, v_2, v_3, v_7\}\) define un isomorfismo.

**Desarrollo:**

1. **Verificación de Grados:** Se calculan las valencias de los vértices en ambos grafos. En \(G_1\), el vértice \(c\) tiene un grado de **2**. Sin embargo, en el mapeo propuesto, \(f(c) = v_1\), y el vértice \(v_1\) en \(G_2\) tiene un grado de **3**.
2. **Preservación de Aristas:** Al analizar la conexión, se observa que en \(G_1\) no existe una arista entre \(a\) y \(c\), pero en \(G_2\) sí existe una arista entre sus imágenes \(v_4\) y \(v_1\).

<div style="border-left: 4px solid #ff9800; padding-left: 16px; margin: 12px 0;">
  <strong>🔍 Conclusión:</strong> La función \(f\) <strong style="color:#d32f2f;">no es un isomorfismo</strong> porque no preserva ni los grados de los vértices ni la estructura de adyacencia.
</div>

**Solución Correcta:** Para un isomorfismo real, se debe usar una función \(g\) que empareje correctamente los grados: \(g(b)=v_5\) (ambos grado 5), y los de grado 2 y 3 según sus conexiones específicas.

---

### 🧩 Ejercicio 2: Demostración Inductiva de la Fórmula de Euler

**Planteamiento:** Demostrar que para todo grafo plano conectado se cumple \(V - A + C = 2\).

**Desarrollo:**

1. **Caso Base:** Un grafo con un solo vértice y 0 aristas. Aquí \(V=1, A=0, C=1\) (la región exterior). Entonces: \(1 - 0 + 1 = 2\). Se cumple.
2. **Hipótesis Inductiva:** Asumimos que la fórmula es válida para un grafo con \(k\) aristas (\(V - k + C = 2\)).
3. **Paso Inductivo (Añadir arista \(k+1\)):**
   - **Escenario A:** La nueva arista conecta un vértice existente con uno nuevo. \(V\) aumenta en 1 y \(A\) aumenta en 1. La ecuación queda \((V+1) - (k+1) + C = V - k + C = 2\).
   - **Escenario B:** La nueva arista conecta dos vértices ya existentes, cerrando un ciclo. \(A\) aumenta en 1 y \(C\) (caras) aumenta en 1. La ecuación queda \(V - (k+1) + (C+1) = V - k + C = 2\).

<div style="border-left: 4px solid #4caf50; padding-left: 16px; margin: 12px 0;">
  <strong>🔍 Conclusión:</strong> En ambos casos la relación se mantiene, demostrando la <strong style="color:#2e7d32;">validez universal</strong> de la fórmula para grafos planos.
</div>

---

### 🧩 Ejercicio 3: Teorema del Triángulo Monocromático en \(K_6\)

**Planteamiento:** Demostrar que si se colorean las aristas de un grafo completo de 6 vértices (\(K_6\)) con dos colores (rojo y azul), siempre existirá un triángulo de un solo color.

**Desarrollo:**

1. **Principio del Palomar:** Seleccionamos un vértice cualquiera \(v\). En \(K_6\), \(v\) tiene 5 aristas incidentes. Al haber solo 2 colores, al menos **3 aristas** deben tener el mismo color (digamos rojo).
2. **Análisis de Vecinos:** Sean \(v_1, v_2, v_3\) los vértices conectados a \(v\) por aristas rojas. Analizamos las aristas entre ellos: \(\{v_1, v_2\}, \{v_2, v_3\}, \{v_1, v_3\}\).
3. **Casuística:**
   - Si **alguna** de estas tres aristas es roja (ej. \(\{v_1, v_2\}\)), se forma un triángulo rojo con \(v\) (\(v-v_1-v_2\)).
   - Si **ninguna** es roja, entonces las tres deben ser azules, formando un triángulo azul entre ellas (\(v_1-v_2-v_3\)).

<div style="border-left: 4px solid #4caf50; padding-left: 16px; margin: 12px 0;">
  <strong>🔍 Conclusión:</strong> La existencia de un triángulo monocromático es <strong style="color:#2e7d32;">inevitable</strong> en \(K_6\).
</div>

---

### 🧩 Ejercicio 4: Ejecución del Algoritmo de Dijkstra

**Planteamiento:** Hallar la ruta más corta entre el nodo **A** y el nodo **G** en un grafo ponderado.

**Desarrollo Paso a Paso:**

1. **Inicialización:** Etiqueta de \(A = 0\), los demás \(\infty\). Conjunto permanente: \(\emptyset\).
2. **Paso 1:** Se elige **A** (mínimo 0). Relajación de vecinos: \(B\) pasa a 3 (\(0+3\)) y \(C\) pasa a 2 (\(0+2\)). Permanente: \(\{A\}\).
3. **Paso 2:** El menor no permanente es **C** (2). Relajación de su vecino \(F\): \(2+5=7\). Permanente: \(\{A, C\}\).
4. **Paso 3:** El menor es **B** (3). Relajación de vecinos: \(D\) pasa a 7 (\(3+4\)) y \(E\) pasa a 5 (\(3+2\)). Permanente: \(\{A, C, B\}\).
5. **Paso 4:** El menor es **E** (5). Relajación de su vecino \(G\): \(5+3=8\). Permanente: \(\{A, C, B, E\}\).
6. **Paso 5:** Se procesan \(D\) y \(F\) (ambos costo 7). No mejoran la distancia de \(G\) (ruta por \(F\) sería \(7+2=9\), mayor que 8).

<div style="border-left: 4px solid #4caf50; padding-left: 16px; margin: 12px 0;">
  <strong>✅ Resultado:</strong> El camino mínimo es <strong>A → B → E → G</strong> con un costo total de <strong style="color:#2e7d32;">8</strong>.
</div>

---

### 🧩 Ejercicio 5: Recorridos BFS y DFS (Búsqueda en Grafos)

**Planteamiento:** Documentar el orden de descubrimiento de nodos en un grafo conectado empezando desde el nodo **A**.

**Desarrollo BFS (Anchura):**
- Utiliza una **cola (FIFO)**. Se visita \(A\), luego sus vecinos directos \(B\) y \(C\). Después se visitan los vecinos de \(B\) (\(D, E\)) y luego los de \(C\) (\(F\)). Finalmente los de \(E\) (\(G\)).
- **Orden:** `A → B → C → D → E → G → F`

**Desarrollo DFS (Profundidad):**
- Utiliza una **pila (LIFO)**. Se explora una rama lo más profundo posible: \(A \to B \to D\). Al llegar a un tope (nodo hoja), se hace *backtracking* a \(B\) y se explora \(E\), luego \(G\), luego \(F\) y finalmente \(C\).
- **Orden:** `A → B → D → E → G → F → C`

<div style="border-left: 4px solid #2196f3; padding-left: 16px; margin: 12px 0;">
  <strong>📌 Nota:</strong> BFS es ideal para encontrar la ruta más corta en grafos no ponderados, mientras que DFS es útil para resolver problemas de backtracking y exploración de todas las soluciones posibles.
</div>

---

<!-- ============================================ -->
<!--       SECCIÓN: EJERCICIO APLICADO            -->
<!-- ============================================ -->
## 🤖 Ejercicio aplicado en un caso real

### Planteamiento del problema
Se modeló un grupo de 8 amigos donde las aristas representan los años de amistad (peso).

### Análisis con lógica y grafos
- **Vértices:** Ana, Bruno, Carla, Diego, Elena, Felipe, Gaby, Hugo.
- **Conectividad:** El grafo es conectado; no hay integrantes aislados.
- **Caminos Críticos:** Los nodos C, D y F son críticos para la conexión del grupo.

### Resultado del análisis
Mediante el algoritmo de Dijkstra, se determinó que el camino más corto (en años de amistad acumulados) entre Ana y Hugo es `A → B → C → D → E → G → F → H`, con un total de **15 años**.

---

<!-- ============================================ -->
<!--         SECCIÓN: REFLEXIÓN PERSONAL          -->
<!-- ============================================ -->
## 💭 Reflexión personal

### ¿Qué fue lo más difícil de entender?
Diferenciar los recorridos de Euler (aristas) y Hamilton (vértices), y comprender la complejidad NP-completa de estos últimos.

### ¿Qué temas comprendí mejor?
La representación matricial de grafos y cómo el álgebra lineal (potencias de matrices) facilita el conteo de caminos en sistemas computacionales.

### ¿Cómo puedo aplicar la teoría de grafos en mi carrera?
La teoría de grafos permite optimizar infraestructuras de red, diseñar algoritmos de enrutamiento más eficientes (como Dijkstra en GPS) y gestionar bases de datos relacionales.

---

<!-- ============================================ -->
<!--           SECCIÓN: ACTIVIDADES               -->
<!-- ============================================ -->
## 📌 Actividades

<div align="center">
  <table style="border-collapse: collapse; width: 80%;">
    <tr>
      <td style="padding: 14px; text-align: center; border: 1px solid #ddd;">
        <a href="APEU3.md" style="text-decoration: none; font-weight: bold; color: #0366d6;">🔬 Práctico Experimentales</a>
      </td>
      <td style="padding: 14px; text-align: center; border: 1px solid #ddd;">
        <a href="AAU3.md" style="text-decoration: none; font-weight: bold; color: #0366d6;">📖 Autónomas</a>
      </td>
    </tr>
    <tr>
      <td style="padding: 14px; text-align: center; border: 1px solid #ddd;">
        <a href="ACDU3.md" style="text-decoration: none; font-weight: bold; color: #0366d6;">👨‍🏫 Contacto Docente</a>
      </td>
      <td style="padding: 14px; text-align: center; border: 1px solid #ddd;">
        <a href="ESU3.md" style="text-decoration: none; font-weight: bold; color: #0366d6;">📊 Evaluación Sumativa</a>
      </td>
    </tr>
  </table>
</div>

---

<!-- ============================================ -->
<!--       SECCIÓN: REGRESAR (BOTÓN ESTILIZADO)   -->
<!-- ============================================ -->
<p align="center" id="regresar">
  <a href="Portafolio.md" style="display: inline-block; padding: 10px 28px; background-color: #0366d6; color: #ffffff; text-decoration: none; border-radius: 6px; font-weight: bold;">
    🔙 Regresar al portafolio
  </a>
</p>
