## Índice

- [Resumen teórico](#resumen-teórico)
- [Ejercicios resueltos](#ejercicios-resueltos)
- [Ejercicio aplicado en un caso real](#ejercicio-aplicado-en-un-caso-real)
- [Reflexión personal](#reflexión-personal)
- [Actividades](#actividades) 


---

## Resumen teórico

### Definición de proposición

Una **proposición** es una entidad lógica que puede clasificarse como verdadera (1) o falsa (0). Se divide en:

- **Simples:** Enunciados únicos e indivisibles que no contienen conectores lógicos (ejemplo: \(x > 5\)).
- **Compuestas:** Resultan de unir dos o más proposiciones simples mediante conectores; su valor de verdad depende de sus componentes.

### Conectores Lógicos

Son elementos encargados de unir proposiciones:

| Conector | Símbolo | Significado | Lenguaje natural |
|----------|---------|-------------|-------------------|
| Negación | \(\neg\) | Invierte el valor de verdad | “no”, “es falso que”, “no es cierto que” |
| Conjunción | \(\land\) | Verdadera solo si ambas son verdaderas | “y”, “pero”, “además”, “también” |
| Disyunción | \(\lor\) | Falsa solo si ambas son falsas | “o” |
| Condicional | \(\rightarrow\) | Falso solo si el primero es verdadero y el segundo falso | “si … entonces” |
| Bicondicional | \(\leftrightarrow\) | Verdadera si ambos valores son iguales | “si y solo si” |

### Tablas de verdad

Es una herramienta que sirve para determinar el valor de verdad de una proposición compuesta considerando todos los casos posibles. El número de filas se calcula con la fórmula \(2^n\), donde \(n\) es el número de proposiciones simples.

**Ejemplo:** \((p \land q) \land (\neg p \lor \neg q)\)

| \(p\) | \(q\) | \(\neg p\) | \(\neg q\) | \(p \land q\) | \(\neg p \lor \neg q\) | \((p \land q) \land (\neg p \lor \neg q)\) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | 1 | 0 | 0 | 1 | 0 | 0 |
| 1 | 0 | 0 | 1 | 0 | 1 | 0 |
| 0 | 1 | 1 | 0 | 0 | 1 | 0 |
| 0 | 0 | 1 | 1 | 0 | 1 | 0 |

### Principales leyes lógicas

Estas establecen **equivalencias lógicas** (\(\equiv\)), lo que significa que ambos lados de la relación siempre tienen el mismo valor de verdad.

| Ley | Fórmula |
|-----|---------|
| **Idempotencia** | \(p \land p \equiv p\) / \(p \lor p \equiv p\) |
| **Conmutativa** | \(p \land q \equiv q \land p\) / \(p \lor q \equiv q \lor p\) |
| **Asociativa** | \((p \land q) \land r \equiv p \land (q \land r)\) / \((p \lor q) \lor r \equiv p \lor (q \lor r)\) |
| **Distributiva** | \(p \land (q \lor r) \equiv (p \land q) \lor (p \land r)\) / \(p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)\) |
| **Doble negación** | \(\neg (\neg p) \equiv p\) |
| **Identidad** | \(p \land V \equiv p\), \(p \lor F \equiv p\), \(p \lor V \equiv V\), \(p \land F \equiv F\) |
| **Complemento** | \(p \lor \neg p \equiv V\), \(p \land \neg p \equiv F\) |
| **Condicional** | \(p \rightarrow q \equiv \neg p \lor q\) |
| **Bicondicional** | \(p \leftrightarrow q \equiv (p \rightarrow q) \land (q \rightarrow p)\) |
| **Absorción** | \(p \land (p \lor q) \equiv p\), \(p \lor (p \land q) \equiv p\) |
| **De Morgan** | \(\neg (p \land q) \equiv \neg p \lor \neg q\), \(\neg (p \lor q) \equiv \neg p \land \neg q\) |

### Principales reglas de inferencia

A diferencia de las leyes, estas formas válidas de razonamiento permiten extraer una conclusión a partir de premisas dadas.

| Regla | Forma |
|-------|-------|
| **Modus Ponendo Ponens (MPP)** | \(p \rightarrow q,\ p \therefore q\) |
| **Modus Tollendo Tollens (MTT)** | \(p \rightarrow q,\ \neg q \therefore \neg p\) |
| **Silogismo disyuntivo** | \(p \lor q,\ \neg p \therefore q\) |
| **Silogismo hipotético puro** | \(p \rightarrow q,\ q \rightarrow r \therefore p \rightarrow r\) |
| **Adjunción** | \(p,\ q \therefore p \land q\) |
| **Simplificación** | \(p \land q \therefore p\) (y también \(\therefore q\)) |
| **Adición** | \(p \therefore p \lor q\) |

---

## Ejercicios resueltos

### Ejercicio 1

\[
[(¬p \lor q) \land (r \rightarrow ¬q) \land r] \equiv ¬p
\]

**Desarrollo:**

- \(r \land (r \rightarrow ¬q) \equiv ¬q\) — Modus Ponens (MP)
- \((¬p \lor q) \land ¬q \equiv ¬p\) — Silogismo Disyuntivo (SD)
- **Resultado:** \(\neg p\)

**Tabla de verdad**

| \(p\) | \(q\) | \(r\) | \(\neg p\) | \(\neg q\) | \(\neg p \lor q\) | \(r \rightarrow \neg q\) | Resultado | \(\neg p\) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | V | F | F | V | F | F | F |
| V | V | F | F | F | V | V | F | F |
| V | F | V | F | V | F | V | F | F |
| V | F | F | F | V | F | V | F | F |
| F | V | V | V | F | V | F | F | V |
| F | V | F | V | F | V | V | F | V |
| F | F | V | V | V | V | V | V | V |
| F | F | F | V | V | V | V | F | V |

**Conclusión:** Contingencia – **Inválida**

---

### Ejercicio 2

\[
\{[p \land (p \lor q)] \rightarrow (r \rightarrow s) \land r \land \neg s\} \equiv p
\]

**Desarrollo:**

- \([p \land (p \lor q)] \equiv p\) — Ley de Absorción
- \((r \rightarrow s) \land r \equiv s\) — Modus Ponens (MP)
- \(s \land \neg s \equiv F\) — Ley de Contradicción
- \(p \rightarrow F \equiv \neg p \lor F\) — Definición de Implicación
- \(\neg p \lor F \equiv \neg p\) — Ley de Identidad
- **Resultado:** \(\neg p\) (Inválido)

**Tabla de verdad**

| \(p\) | \(q\) | \(r\) | \(s\) | Antecedente: \([p \land (p \lor q)]\) | Consecuente: \((r \rightarrow s) \land r \land \neg s\) | Resultado (Argumento) | Conclusión: \(\neg p\) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | V | V | V | F | F | F |
| V | V | V | F | V | F | F | F |
| V | V | F | V | V | F | F | F |
| V | V | F | F | V | F | F | F |
| V | F | V | V | V | F | F | F |
| V | F | V | F | V | F | F | F |
| V | F | F | V | V | F | F | F |
| V | F | F | F | V | F | F | F |
| F | V | V | V | F | F | V | V |
| F | V | V | F | F | F | V | V |
| F | V | F | V | F | F | V | V |
| F | V | F | F | F | F | V | V |
| F | F | V | V | F | F | V | V |
| F | F | V | F | F | F | V | V |
| F | F | F | V | F | F | V | V |
| F | F | F | F | F | F | V | V |

**Conclusión:** Contingencia – **Inválida**

---

### Ejercicio 3

\[
(p \land q \land r) \lor (p \land q \land \neg r) \lor (p \land \neg q) \equiv p
\]

**Desarrollo de simplificación:**

- \([(p \land q) \land (r \lor \neg r)] \lor (p \land \neg q)\) — Ley Distributiva
- \([(p \land q) \land V] \lor (p \land \neg q)\) — Ley del Tercero Excluido
- \((p \land q) \lor (p \land \neg q)\) — Ley de Identidad
- \(p \land (q \lor \neg q)\) — Ley Distributiva
- \(p \land V\) — Ley del Tercero Excluido
- **Resultado:** \(p\) — Ley de Identidad

**Tabla de verdad**

| \(p\) | \(q\) | \(r\) | \(\neg r\) | \(\neg q\) | \(p \land q \land r\) | \(p \land q \land \neg r\) | \(p \land \neg q\) | Resultado Final | \(p\) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | V | F | F | V | F | F | V | V |
| V | V | F | V | F | F | V | F | V | V |
| V | F | V | F | V | F | F | V | V | V |
| V | F | F | V | V | F | F | V | V | V |
| F | V | V | F | F | F | F | F | F | F |
| F | V | F | V | F | F | F | F | F | F |
| F | F | V | F | V | F | F | F | F | F |
| F | F | F | V | V | F | F | F | F | F |

**Conclusión:** Contingencia – **Válida**

---

### Ejercicio 4

\[
[(p \lor q) \land \neg p] \land (r \lor p) \equiv q \land \neg p \land r
\]

**Desarrollo de simplificación:**

- \([(p \land \neg p) \lor (q \land \neg p)] \land (r \lor p)\) — Ley Distributiva
- \([F \lor (q \land \neg p)] \land (r \lor p)\) — Ley de Contradicción
- \((q \land \neg p) \land (r \lor p)\) — Ley de Identidad
- \(q \land [\neg p \land (r \lor p)]\) — Ley Asociativa
- \(q \land [(\neg p \land r) \lor (\neg p \land p)]\) — Ley Distributiva
- \(q \land [(\neg p \land r) \lor F]\) — Ley de Contradicción
- **Resultado:** \(q \land \neg p \land r\) — Ley de Identidad

**Tabla de verdad**

| \(p\) | \(q\) | \(r\) | \(\neg p\) | \(p \lor q\) | \((p \lor q) \land \neg p\) | \(r \lor p\) | Resultado Final | \(q \land \neg p \land r\) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | V | F | V | F | V | F | F |
| V | V | F | F | V | F | V | F | F |
| V | F | V | F | V | F | V | F | F |
| V | F | F | F | V | F | V | F | F |
| F | V | V | V | V | V | V | V | V |
| F | V | F | V | V | V | F | F | F |
| F | F | V | V | F | F | V | F | F |
| F | F | F | V | F | F | F | F | F |

**Conclusión:** Contingencia – **Válida**

---

### Ejercicio 5

\[
\neg(p \rightarrow q) \lor (p \land q \land r) \equiv p \land (\neg q \lor r)
\]

**Desarrollo de simplificación:**

- \(\neg(\neg p \lor q) \lor (p \land q \land r)\) — Definición de Implicación
- \((p \land \neg q) \lor (p \land q \land r)\) — Ley de De Morgan e Involución
- \(p \land [\neg q \lor (q \land r)]\) — Ley Distributiva
- \(p \land [(\neg q \lor q) \land (\neg q \lor r)]\) — Ley Distributiva (interna)
- \(p \land [V \land (\neg q \lor r)]\) — Ley del Tercero Excluido
- **Resultado:** \(p \land (\neg q \lor r)\) — Ley de Identidad

**Tabla de verdad**

| \(p\) | \(q\) | \(r\) | \(\neg q\) | \(p \rightarrow q\) | \(\neg(p \rightarrow q)\) | \(p \land q \land r\) | Resultado Final | \(\neg q \lor r\) | \(p \land (\neg q \lor r)\) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| V | V | V | F | V | F | V | V | V | V |
| V | V | F | F | V | F | F | F | F | F |
| V | F | V | V | F | V | F | V | V | V |
| V | F | F | V | F | V | F | V | V | V |
| F | V | V | F | V | F | F | F | V | F |
| F | V | F | F | V | F | F | F | F | F |
| F | F | V | V | V | F | F | F | V | F |
| F | F | F | V | V | F | F | F | V | F |

**Conclusión:** Contingencia – **Válida**

---

## Ejercicio aplicado en un caso real

### Planteamiento del problema

En una clase de robótica educativa, los estudiantes deben programar un robot esférico (Sphero Mini) para que ejecute una acción de alerta (cambiar de color) solo cuando se cumplan simultáneamente dos condiciones físicas detectadas por sus sensores (un acelerómetro y un giroscopio).

### Definición de proposiciones

- **\(p\):** El robot está rodando hacia adelante.
- **\(q\):** El sensor detecta un choque o colisión.
- **\(r\):** El robot enciende sus luces.

### Expresión simbólica

La metodología del proyecto se describe como:

\[
(p \land q) \rightarrow r
\]

Traducción al lenguaje natural: *“Si el robot está rodando y detecta un choque, entonces se enciende la luz roja”*.

### Análisis con lógica proposicional

En la segunda fase, el estudiante debe entender el comportamiento de la implicación en diferentes casos:

- **a)** Si el robot solo rueda, pero no choca (\(p\) es V, \(q\) es F), la luz no enciende.
- **b)** Si el robot está quieto, pero alguien lo golpea (\(p\) es F, \(q\) es V), la luz tampoco se enciende.
- **c)** La acción \(r\) solo es obligatoria para el programa cuando ambas condiciones son verdaderas al mismo tiempo.

### Conclusión de resultados

Este tipo de ejercicios prácticos permite que el aprendizaje no sea solo teórico. Al final del experimento, los estudiantes lograron mejorar sus aprendizajes en **0.97 puntos** en promedio. La lógica matemática se vuelve clave para la comprensión de conceptos abstractos necesarios en programación.

---

## Reflexión personal

### ¿Qué fue lo más difícil de entender?

El mayor desafío consistió en identificar el contexto de aplicación preciso para cada ley lógica y regla de inferencia. Mediante la práctica constante, he optimizado mi razonamiento matemático en la resolución de ejercicios.

### ¿Qué temas comprendí mejor?

Comprendí con precisión la estructura de las tablas de verdad, logrando clasificar sus funciones y reconocer patrones lógicos en las soluciones finales.

### ¿Cómo puedo aplicar la lógica en mi carrera?

La lógica constituye el lenguaje de bajo nivel fundamental para el control de flujo en estructuras condicionales y ciclos. Su aplicación permite optimizar algoritmos mediante la reducción de comparaciones redundantes, elevando la calidad técnica y la eficiencia en el desarrollo de software.

---
## actividades

- [Actividades Practico Experimentales](APEU1.md)
- [Actividades Autonomas](AAU1.md)
- [Actividad Contacto Docente](ACDU1.md)
- [Evaluacion Sumativa](ESU1.md)

[Regresar](Portafolio.md)
