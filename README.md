# Algorithms & Data Structures Roadmap

Guía interactiva de **Algoritmos y Estructuras de Datos** (UTN Facultad Regional Buenos Aires), armada a partir de las clases grabadas de la materia y los apuntes de cátedra.

Es un único archivo HTML autocontenido: se abre con doble clic, funciona sin internet, sin instalación y sin dependencias.

> **Ver la guía online:** https://TU-USUARIO.github.io/algorithms-data-structures-roadmap/

---

## La idea

La materia parece una pila de temas sueltos, pero tiene una sola idea adentro: **los patrones algorítmicos no cambian, lo único que cambia de una estructura a otra es cómo se accede al dato.**

| Estructura | Dónde vive | Llegar al elemento *n* | Avanzar al siguiente |
|---|---|---|---|
| Vector | Memoria | `v[n]` | `i++` |
| Archivo | Disco | `fseek(f, n*sizeof(reg), SEEK_SET)` | el propio `fread` |
| Lista | Memoria, pedida en ejecución | recorriendo desde el principio | `p = p->sig` |

Esa tabla es el resumen de la materia. Todo lo demás es aprender a elegir cuál de las tres conviene y aplicarle los patrones de siempre.

## Cómo está organizada

Cinco partes que se leen de corrido. Cada una abre explicando qué necesita de la anterior y cierra indicando qué sigue.

1. **El dato y su forma** — tipos, structs y punteros.
2. **Vectores** — los cuatro patrones: ordenar, buscar, aparear y cortar por grupo.
3. **Archivos** — los mismos patrones cuando el dato vive en disco.
4. **Memoria dinámica** — listas, lista de listas, pilas y colas.
5. **Integración** — parciales y un final resuelto punto por punto.

## Qué incluye

- **Trece figuras interactivas** que se ejecutan paso a paso: burbuja, búsqueda binaria, apareo de vectores y de archivos, corte de control, punteros en memoria, pasaje por valor y por referencia, `fseek`/`ftell`, insertar ordenado en una lista, pila con auxiliar, y la construcción de una lista de listas registro por registro.
- **Un caso completo explicado función por función**: un programa que lee `ALUMNOS.DAT` y arma una lista de divisiones con sublistas de alumnos, con el análisis de cada función, diagramas de memoria y los errores típicos que hacen perder puntos.
- **Archivos a fondo**: `fopen` y sus modos, lectura anticipada, `feof`, acceso directo, la función `cantReg`, los cinco pasos para modificar un registro y el apareo directo entre archivos.
- **Un final real resuelto** (06/03/2023) con las soluciones colapsables para intentarlas antes de mirar.
- Términos con definición al pasar el cursor, autoevaluaciones, barra de progreso, y modo claro / noche.

## Cómo usarlo

Descargá o cloná el repo y abrí `index.html` en cualquier navegador:

```bash
git clone https://github.com/TU-USUARIO/algorithms-data-structures-roadmap.git
```

También podés usarlo online desde el enlace de arriba.

## Sobre las fuentes

La guía se construyó a partir de las transcripciones de las clases grabadas del curso, los apuntes de cátedra (Unidades 01 a 10, Dr. Oscar Bruno) y exámenes de años anteriores.

**Ese material no se incluye en este repositorio**, por dos razones: no es de mi autoría y las transcripciones contienen intervenciones de docentes y compañeros de cursada. Acá se publica únicamente la guía, que es una elaboración propia sobre esos contenidos.

Si algo de lo explicado no coincide con lo que se dictó, manda siempre lo que diga la cátedra.

## Stack

Nada. HTML, CSS y JavaScript en un solo archivo, sin frameworks, sin build, sin CDN. Los diagramas son SVG generados a mano y por script; el tema se maneja con variables CSS.

---

*Hecho para cursar y aprobar AyED. Si te sirve, dejá una estrella.*
