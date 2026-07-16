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
<!--          ENCABEZADO DE LA UNIDAD 3            -->
<!-- ============================================ -->
## 📂 Unidad 3: Árboles, Grafos y Estructuras de Datos

> En la arquitectura de la computación moderna, los árboles y grafos no solo actúan como contenedores de información, sino como el núcleo determinante de la eficiencia algorítmica. Esta unidad evalúa los compromisos algorítmicos (*trade-offs*) entre diversas estructuras jerárquicas, analizando sus fundamentos teóricos y la rigurosidad de los recorridos sistemáticos.

---

<!-- ============================================ -->
<!--                  ÍNDICE MEJORADO              -->
<!-- ============================================ -->
## 📑 Índice

<table align="center" style="border-collapse: collapse; width: 85%;">
  <tr>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#introducción-y-marco-estratégico" style="text-decoration: none; font-weight: bold; color: #0366d6;">🎯 Introducción</a>
    </td>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#resumen-teórico" style="text-decoration: none; font-weight: bold; color: #0366d6;">📘 Resumen teórico</a>
    </td>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#optimización-y-compresión" style="text-decoration: none; font-weight: bold; color: #0366d6;">📊 Optimización</a>
    </td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#metodología-de-recorridos" style="text-decoration: none; font-weight: bold; color: #0366d6;">🔄 Recorridos</a>
    </td>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#ejercicios-resueltos" style="text-decoration: none; font-weight: bold; color: #0366d6;">📝 Ejercicios resueltos</a>
    </td>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;">
      <a href="#reflexión-personal" style="text-decoration: none; font-weight: bold; color: #0366d6;">💭 Reflexión</a>
    </td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center; border: 1px solid #ddd;" colspan="3">
      <a href="#actividades" style="text-decoration: none; font-weight: bold; color: #0366d6;">📌 Actividades</a> &nbsp;|&nbsp; 
      <a href="#regresar" style="text-decoration: none; font-weight: bold; color: #0366d6;">🔙 Regresar</a>
    </td>
  </tr>
</table>

---

<!-- ============================================ -->
<!--       SECCIÓN 1: INTRODUCCIÓN ESTRATÉGICA    -->
<!-- ============================================ -->
## 🎯 Introducción y Marco Estratégico

La transición de estructuras lineales a jerárquicas permite modelar la complejidad inherente de sistemas de archivos, redes de comunicación y motores de inferencia. El objetivo primordial de este portafolio es evaluar los compromisos algorítmicos (*trade-offs*) entre diversas estructuras jerárquicas, analizando sus fundamentos teóricos, la mecánica de los códigos de prefijos y la rigurosidad de los recorridos sistemáticos para maximizar la velocidad de recuperación y procesamiento de datos.

---

<!-- ============================================ -->
<!--             SECCIÓN: RESUMEN TEÓRICO          -->
<!-- ============================================ -->
## 📘 Resumen Teórico: Fundamentos de Árboles y Grafos

Como especialistas, entendemos que la implementación técnica carece de validez sin una formalización matemática previa. La robustez de un sistema depende de la adherencia a las propiedades estructurales que garantizan la predictibilidad del algoritmo.

### 🔹 Definición y Propiedades Críticas del Árbol

Un **árbol** es un grafo conexo acíclico. Para un conjunto de \(n\) nodos, se deben cumplir estrictamente las siguientes propiedades:

1. **Conectividad:** Existe al menos un camino entre cualquier par de vértices.
2. **Aciclicidad:** La estructura prohíbe la existencia de circuitos cerrados; la adición de una sola arista crearía un ciclo.
3. **Minimalidad de Aristas:** Un árbol posee exactamente \(n-1\) aristas.
4. **Unicidad de Trayectoria:** Existe un único camino simple entre cualquier par de nodos.
5. **Vulnerabilidad Estructural:** La eliminación de cualquier arista resulta en un grafo no conexo.

### 🔹 Tipos de Árboles y su Justificación Técnica

| Tipo | Descripción |
| :--- | :--- |
| **Árbol Libre** | Grafo conexo sin raíz designada. |
| **Árbol Enraizado** | Establece una jerarquía clara mediante un nodo raíz. |
| **Árbol Binario** | Restringe el grado de salida a un máximo de 2, facilitando búsquedas dicotómicas. |
| **Árbol Binario Completo** | Optimiza el uso de memoria al llenar niveles de izquierda a derecha. |
| **Árbol Binario Perfecto** | Estructura ideal donde todas las hojas residen en el mismo nivel. |
| **Árbol Balanceado** | Mitiga la degradación del rendimiento al mantener una diferencia mínima de altura. |
| **Árbol AVL** | Estabiliza el rendimiento mediante autorrotaciones para prevenir el peor escenario de \(O(n)\). |
| **Árbol B y B+** | Estructuras multicamino esenciales para minimizar las operaciones de E/S (*Disk I/O*) en sistemas de archivos y bases de datos masivas. |

### 🔹 Fundamentos de Grafos y Conectividad

La teoría de grafos define el **Orden** como el número de vértices y el **Tamaño** como el número de aristas. El **Grado** de un nodo determina su conectividad.

- **Caminos de Euler:** Un grafo conexo admite un camino de Euler si y solo si posee exactamente dos vértices de grado impar.
- **Circuitos de Hamilton:** Se enfocan en visitar cada vértice exactamente una vez. Su resolución es un problema **NP-completo**, lo que subraya la necesidad de heurísticas en la optimización de rutas.

---

<!-- ============================================ -->
<!--        SECCIÓN: OPTIMIZACIÓN Y COMPRESIÓN     -->
<!-- ============================================ -->
## 📊 Optimización y Compresión: Código de Huffman y Árboles de Búsqueda

La ingeniería de software contemporánea exige el equilibrio entre la densidad de almacenamiento y la latencia de acceso.

### 🔹 Código de Huffman (Compresión de Datos)

El algoritmo de Huffman es un método de codificación estadística de longitud variable. Al asignar códigos binarios cortos a símbolos de alta frecuencia y códigos largos a los infrecuentes, se logra una compresión sin pérdidas. Su propiedad de **código de prefijo** asegura que ningún código sea el inicio de otro, garantizando una decodificación unívoca. Es el pilar de formatos como ZIP, JPEG, PNG, MP3 y algoritmos de compresión de texto.

### 🔹 Árboles de Búsqueda Binaria (ABB) y Balanceo

Un ABB impone un orden total: hijos menores a la izquierda, mayores a la derecha. Sin embargo, una inserción secuencial puede convertirlo en una lista ligada (\(O(n)\)). El **balanceo AVL** interviene mediante rotaciones que mitigan la asimetría y estabilizan el acceso a \(O(\log n)\), previniendo cuellos de botella en la indexación de bases de datos.

### 🔹 Comparativa de Estructuras Especializadas

| Estructura | Lógica de Reequilibrio | Determinante de Altura | Aplicación |
| :--- | :--- | :--- | :--- |
| **Heaps** | Propiedad de montón vía *Sift-up/Sift-down*. | Logarítmica respecto a \(n\). | Colas de prioridad (Dijkstra). |
| **Tries** | Navegación por prefijos de caracteres. | Longitud de la clave (\(L\)), no \(n\). | Autocompletado, enrutamiento IP. |
| **Árboles B** | División y fusión de nodos multicamino. | Mínima (estructura plana). | Bases de datos a gran escala. |

---

<!-- ============================================ -->
<!--       SECCIÓN: METODOLOGÍA DE RECORRIDOS     -->
<!-- ============================================ -->
## 🔄 Metodología de Recorridos en Árboles Binarios

Para el procesamiento determinista de nodos en compiladores y motores de búsqueda, aplicamos la siguiente lógica algorítmica:

| Recorrido | Orden de Visita | Uso Típico |
| :--- | :--- | :--- |
| **Preorden (NID)** | 1. Visitar Raíz → 2. Subárbol Izquierdo → 3. Subárbol Derecho. | Duplicación de estructuras y expresiones prefijas. |
| **Inorden (IND)** | 1. Subárbol Izquierdo → 2. Visitar Raíz → 3. Subárbol Derecho. | Recuperación de datos en orden ascendente. |
| **Postorden (IDN)** | 1. Subárbol Izquierdo → 2. Subárbol Derecho → 3. Visitar Raíz. | Eliminación de nodos (liberación de memoria) y evaluación de expresiones postfijas. |

---

<!-- ============================================ -->
<!--           SECCIÓN: EJERCICIOS RESUELTOS      -->
<!-- ============================================ -->
## 📝 Desarrollo: Resolución Detallada de Ejercicios Prácticos

---

### 🧩 Ejercicio 1: Inventario de Tienda de Tecnología

**Datos de entrada:** \([45, 23, 65, 12, 38, 52, 90]\)

**Arquitectura del Árbol:**
- **45** es la raíz.
- **23** (< 45) va a la izquierda; **65** (> 45) va a la derecha.
- **12** y **38** cuelgan de **23**; **52** y **90** cuelgan de **65**.

**Resultados de Recorrido:**

| Recorrido | Secuencia Resultante |
| :--- | :--- |
| **Preorden** | `[45, 23, 12, 38, 65, 52, 90]` |
| **Inorden** | `[12, 23, 38, 45, 52, 65, 90]` |
| **Postorden** | `[12, 38, 23, 52, 90, 65, 45]` |

<div style="border-left: 4px solid #4caf50; padding-left: 16px; margin: 12px 0;">
  <strong>✅ Verificación:</strong> El recorrido <strong>Inorden</strong> devuelve los elementos perfectamente ordenados de menor a mayor, validando la correcta inserción en el ABB.
</div>

---

### 🧩 Ejercicio 2: Estación Meteorológica (Temperaturas)

**Datos de entrada:** \([18, 24, 15, 20, 28, 16]\)

**Lógica de Inserción:**
- **18** (Raíz) → **15** (Izq), **24** (Der).
- **16** cuelga a la derecha de **15**.
- **20** (Izq) y **28** (Der) cuelgan de **24**.

**Resultados:**

| Recorrido | Secuencia Resultante |
| :--- | :--- |
| **Inorden** (Reporte ordenado) | `[15, 16, 18, 20, 24, 28]` |
| **Postorden** | `[16, 15, 20, 28, 24, 18]` |

---

### 🧩 Ejercicio 3: Triage Médico de Alta Complejidad (14 Nodos)

**Secuencia de inserción:** \([60, 35, 75, 20, 45, 70, 85, 10, 28, 40, 50, 65, 80, 95]\)

**Lógica de Resolución Rigurosa:**
- **Preorden (NID):** Se anota cada nodo al contacto inicial descendente. Raíz **60** → subárbol **35** (20 → 10, 28) → subárbol **45** (40, 50) → subárbol **75** (70 → 65) → subárbol **85** (80, 95).
  - **Resultado:** `[60, 35, 20, 10, 28, 45, 40, 50, 75, 70, 65, 85, 80, 95]`
- **Inorden (IND):** Para obtener el nodo **35**, el algoritmo debe agotar recursivamente el extremo izquierdo profundo (10), ascender al padre (20), procesar su derecha (28) y finalmente subir a 35. Este rigor garantiza el ordenamiento clínico.
  - **Resultado:** `[10, 20, 28, 35, 40, 45, 50, 60, 65, 70, 75, 80, 85, 95]`

<div style="border-left: 4px solid #2196f3; padding-left: 16px; margin: 12px 0;">
  <strong>📌 Nota:</strong> El recorrido <strong>Inorden</strong> en un ABB siempre produce una lista totalmente ordenada, lo que resulta crucial para reportes clínicos y estadísticos.
</div>

---

### 🧩 Ejercicio 4: Estructura por Niveles con Nombres

**Datos por nivel de profundidad:**
- **Nivel 1:** Erika
- **Nivel 2:** Martha, Andrea
- **Nivel 3:** Alicia, Francisco, Alma, Martín
- **Nivel 4:** Juan

**Análisis:** La eficiencia del recorrido es **agnóstica al tipo de dato** (*string* / *int*), dependiendo exclusivamente de la topología del árbol.

**Recorrido Inorden resultante:** `[Juan, Alicia, Martha, Francisco, Erika, Alma, Andrea, Martín]`

---

### 🧩 Ejercicio 5: Representación de Grafos y Algoritmo de Dijkstra

Para hallar rutas mínimas, el algoritmo de Dijkstra se restringe estrictamente a pesos no negativos. Su implementación digital se apoya en:

1. **Matriz de Adyacencia:** Permite calcular el número de caminos de longitud \(k\) elevando la matriz a la potencia \(A^k\).
2. **Matriz de Incidencia:** Documenta la relación entre vértices y aristas, facilitando el análisis de conectividad en infraestructuras de gran escala.

<div style="border-left: 4px solid #ff9800; padding-left: 16px; margin: 12px 0;">
  <strong>⚙️ Aplicación:</strong> Dijkstra es fundamental en sistemas de navegación GPS y enrutamiento de redes, donde se requiere la ruta óptima en tiempo real.
</div>

---

<!-- ============================================ -->
<!--         SECCIÓN: REFLEXIÓN PERSONAL          -->
<!-- ============================================ -->
## 💭 Conclusiones y Reflexión Personal

### 🔹 Conclusiones Técnicas

- **Estructura:** Los árboles optimizan la organización al garantizar una única ruta entre nodos, eliminando la redundancia cíclica.
- **Balanceo:** Estructuras como AVL y B-Trees son imperativas para prevenir la degradación del rendimiento en sistemas de producción.
- **Compresión:** Huffman demuestra la elegancia de las matemáticas discretas aplicadas a la transmisión de datos (PNG, MP3).
- **Inteligencia Artificial:** Los Árboles de Decisión constituyen el modelo predictivo jerárquico base para la clasificación y regresión en *Machine Learning*.

### 🔹 Reflexión Personal

> **Abraham Daniel Maza Lapo:**  
> *"Este análisis vinculó la teoría pura con problemas reales. Es la base necesaria para abordar estructuras avanzadas y soluciones de software de alta escala."*

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
