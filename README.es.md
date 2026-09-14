<div align="center">

# Algorithms & Data Structures Roadmap

**Guía interactiva de Algoritmos y Estructuras de Datos, en un solo archivo.**

Armada a partir de las clases grabadas y los apuntes de cátedra de *Algoritmos y Estructuras de Datos*, **UTN Facultad Regional Buenos Aires**. Recorre la materia entera en cinco partes: el dato en memoria, después en disco, y después el dato que crece mientras el programa corre.

[**Abrir la guía →**](https://juanm4ram.github.io/algorithms-data-structures-roadmap/)

![Sin dependencias](https://img.shields.io/badge/dependencias-ninguna-3a6b4c)
![Sin build](https://img.shields.io/badge/build-ninguno-1f5490)
![Un solo archivo](https://img.shields.io/badge/un%20solo%20archivo-HTML-95571c)
![Funciona sin internet](https://img.shields.io/badge/funciona-offline-6d675b)

[English](README.md) · **Español**

<br>

<img src="docs/preview-guia.png" alt="La guía mostrando la apertura de una parte y el hilo conductor de la materia" width="880">

</div>

---

## Vista previa

| Una figura ejecutándose paso a paso | Un programa explicado función por función |
|---|---|
| <img src="docs/preview-figura.png" alt="Figura interactiva ejecutándose paso a paso" width="420"> | <img src="docs/preview-caso.png" alt="Programa completo desglosado función por función" width="420"> |

---

## Índice

- [Qué es](#qué-es)
- [La única idea de toda la materia](#la-única-idea-de-toda-la-materia)
- [Qué incluye](#qué-incluye)
- [Las cinco partes](#las-cinco-partes)
- [Usarla localmente](#usarla-localmente)
- [Stack](#stack)
- [Fuentes y atribución](#fuentes-y-atribución)
- [Contribuir](#contribuir)
- [Licencia](#licencia)

## Qué es

La materia completa metida en **un único archivo HTML**. Sin instalación, sin build, sin dependencias y sin conexión: doble clic y se abre en cualquier navegador.

Cubre todo el programa: vectores y structs, los cuatro patrones algorítmicos, archivos binarios con acceso directo, punteros y memoria dinámica, listas enlazadas, pilas y colas, y dos exámenes reales resueltos paso a paso.

No es un manual de consulta. Está hecha para **leerse en orden**, como un apunte: cada sección abre explicando qué necesita de la anterior y cierra indicando qué sigue.

## La única idea de toda la materia

La materia parece una pila de temas sueltos, pero no lo es. Los patrones algorítmicos no cambian nunca: recorrer, buscar, aparear, cortar por grupo. Lo único que cambia de una estructura a otra es **cómo se accede al dato**.

| Estructura | Dónde vive | Llegar al elemento *n* | Avanzar al siguiente |
|---|---|---|---|
| Vector | Memoria | `v[n]` | `i++` |
| Archivo | Disco | `fseek(f, n*sizeof(reg), SEEK_SET)` | el propio `fread` |
| Lista | Memoria, pedida en ejecución | recorriendo desde el principio | `p = p->sig` |

Esa tabla es el resumen de la materia. Todo lo demás es aprender a elegir cuál de las tres conviene y aplicarle los mismos cuatro patrones. La guía marca ese hilo cada vez que reaparece.

## Qué incluye

**Trece figuras interactivas** que se ejecutan paso a paso con botones, no animaciones para mirar:

| Figura | Qué muestra |
|---|---|
| Burbuja | Cómo decrecen las comparaciones en cada paso |
| Búsqueda binaria | La ventana cerrándose sobre el valor buscado |
| Apareo de vectores | Comparar cabezas y consumir la menor |
| Apareo de archivos | El mismo algoritmo con `fread`/`fwrite` en vez de índices |
| Corte de control | Listado agrupado con subtotales, fila por fila |
| Punteros | Los dos espacios de memoria: la dirección y el valor |
| Valor vs referencia | Por qué uno modifica el original y el otro no |
| `fseek` / `ftell` | Mover el puntero del archivo en bytes |
| Insertar ordenado | Cómo se re-enlazan los punteros en cada uno de los tres casos |
| Pila | Apilar, desapilar, y por qué recuperar implica destruir el nodo |
| Lista de listas | Una estructura de dos niveles construida registro por registro |

**Un programa entero explicado función por función**: leer `ALUMNOS.DAT` y armar una lista de divisiones, cada una con su sublista de alumnos ordenada. Se analizan `main`, `buscar`, `insertarOrdenadoLP`, `insertarSinRepetir`, `insertarOrdenadoLS`, `procesarArchivo`, `mostrarListado` y `liberarListas`, con diagramas de memoria y una tabla de los errores que hacen perder puntos.

**Un final real resuelto** (06/03/2023), con cada punto en un bloque colapsable para intentarlo antes de mirar.

Además: definiciones al pasar el cursor, autoevaluaciones, barra de progreso de lectura y modo claro / noche.

## Las cinco partes

1. **El dato y su forma** — tipos, structs, punteros y quién puede modificar un valor.
2. **Vectores** — los cuatro patrones: ordenar, buscar, aparear y cortar por grupo.
3. **Archivos** — los mismos patrones cuando el dato vive en disco.
4. **Memoria dinámica** — listas, lista de listas, pilas y colas.
5. **Integración** — parciales y final resueltos.

## Usarla localmente

```bash
git clone https://github.com/juanm4ram/algorithms-data-structures-roadmap.git
cd algorithms-data-structures-roadmap
```

Después abrí `index.html` en cualquier navegador. Eso es toda la instalación.

## Stack

HTML, CSS y JavaScript planos en un solo archivo. Sin frameworks, sin bundler, sin CDN, sin fuentes externas. Los diagramas son SVG escritos a mano y generados por script; el tema se maneja con variables CSS, que es también lo que permite que las figuras se lean bien en modo claro y en modo noche.

El archivo es autocontenido a propósito: una guía de estudio que no podés abrir sin Wi-Fi o durante un corte de luz no sirve de mucho.

## Fuentes y atribución

Construida a partir de las transcripciones de las clases grabadas, los apuntes de cátedra (Unidades 01 a 10, Dr. Oscar Bruno) y exámenes de años anteriores.

**Ese material fuente no se incluye en este repositorio, a propósito.** No es de mi autoría y las transcripciones contienen intervenciones de docentes y compañeros de cursada. Lo que se publica acá es la guía, que sí es una elaboración propia sobre esos contenidos.

Si algo de lo explicado no coincide con lo que dice tu docente, mandá siempre lo que diga la cátedra.

## Contribuir

¿Encontraste un error, una errata o una explicación que no se sostiene? Abrí un issue. Las correcciones al contenido técnico son especialmente bienvenidas: esto es material de estudio, y una explicación equivocada es peor que ninguna.

## Licencia

La guía se comparte con fines de estudio bajo [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es): usala, adaptala y compartila libremente, con atribución y sin fines comerciales. El material de cátedra en el que se basa pertenece a sus autores.

---

<div align="center">
<sub>Hecha mientras cursaba la materia. Si te sirve, dejá una estrella.</sub>
</div>
