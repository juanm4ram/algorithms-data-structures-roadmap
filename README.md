<div align="center">

# Algorithms & Data Structures Roadmap

**An interactive, single-file study guide for Algorithms & Data Structures.**

Built from the recorded lectures and course notes of *Algoritmos y Estructuras de Datos* at **UTN Facultad Regional Buenos Aires**. It walks the whole subject in five parts: data in memory, then on disk, then data that grows while the program runs.

[**Open the guide →**](https://juanm4ram.github.io/algorithms-data-structures-roadmap/)

![No dependencies](https://img.shields.io/badge/dependencies-none-3a6b4c)
![No build step](https://img.shields.io/badge/build-none-1f5490)
![Single file](https://img.shields.io/badge/single%20file-HTML-95571c)
![Works offline](https://img.shields.io/badge/works-offline-6d675b)

**English** · [Español](README.es.md)

> **Note:** the guide itself is written in **Spanish**, since it follows an Argentine university course. This README is available in both languages.

<br>

<img src="docs/preview-guia.png" alt="The guide showing a part opening and the running thread of the subject" width="880">

</div>

---

## Preview

| Stepping through a figure | A program explained function by function |
|---|---|
| <img src="docs/preview-figura.png" alt="Interactive figure being executed step by step" width="420"> | <img src="docs/preview-caso.png" alt="Full program broken down function by function" width="420"> |

---

## Table of contents

- [What this is](#what-this-is)
- [The one idea behind the whole subject](#the-one-idea-behind-the-whole-subject)
- [What's inside](#whats-inside)
- [The five parts](#the-five-parts)
- [Running it locally](#running-it-locally)
- [Tech](#tech)
- [Sources and attribution](#sources-and-attribution)
- [Contributing](#contributing)
- [License](#license)

## What this is

A complete course companion packed into **one HTML file**. No installation, no build step, no dependencies, no internet connection required. Double-click it and it opens in any browser.

It covers the full syllabus of a first-year data structures course taught in C/C++: arrays and structs, the four core algorithmic patterns, binary files with direct access, pointers and dynamic memory, linked lists, stacks and queues, and two real exams solved step by step.

It is not a reference manual. It is built to be **read in order**, like a textbook, with each section explaining what it needs from the previous one and what it sets up for the next.

## The one idea behind the whole subject

The course looks like a pile of unrelated topics. It isn't. The algorithmic patterns never change — traverse, search, merge, group. The only thing that changes from one structure to the next is **how you reach the data**.

| Structure | Where it lives | Reaching element *n* | Advancing to the next |
|---|---|---|---|
| Array | Memory | `v[n]` | `i++` |
| File | Disk | `fseek(f, n*sizeof(reg), SEEK_SET)` | `fread` itself |
| Linked list | Memory, allocated at runtime | walk from the head | `p = p->sig` |

That table is the summary of the entire subject. Everything else is learning which of the three to pick, and applying the same four patterns to it. The guide marks this thread explicitly as it recurs.

## What's inside

**Thirteen interactive figures** you step through with buttons, not animations you watch:

| Figure | What it shows |
|---|---|
| Bubble sort | How the comparison count shrinks on every pass |
| Binary search | The window closing in on the target |
| Merge (arrays) | Comparing heads, consuming the smaller one |
| Merge (files) | The same algorithm with `fread`/`fwrite` instead of indices |
| Control break | Grouped listing with subtotals, built row by row |
| Pointers | Two memory cells, the address and the value, line by line |
| By value vs by reference | Why one modifies the original and the other doesn't |
| `fseek` / `ftell` | Moving the file pointer in bytes |
| Ordered insert | How the pointers get relinked on each of the three cases |
| Stack | Push, pop, and why reading destroys the node |
| List of lists | A two-level structure built record by record from a file |

**A full program explained function by function** — reading `ALUMNOS.DAT` into a list of divisions, each with its own sorted sublist of students: `main`, `buscar`, `insertarOrdenadoLP`, `insertarSinRepetir`, `insertarOrdenadoLS`, `procesarArchivo`, `mostrarListado` and `liberarListas`, with memory diagrams and a table of the mistakes that cost marks.

**A real final exam solved** (2023-03-06), each question with a collapsible solution so you can attempt it first.

Plus hover definitions on key terms, self-check questions, a reading-progress bar, and light/dark themes.

## The five parts

1. **Data and its shape** — types, structs, pointers, and who is allowed to modify a value.
2. **Arrays** — the four patterns: sort, search, merge, control break.
3. **Files** — the same patterns once the data lives on disk.
4. **Dynamic memory** — linked lists, lists of lists, stacks and queues.
5. **Integration** — midterm and final exams, solved.

## Running it locally

```bash
git clone https://github.com/juanm4ram/algorithms-data-structures-roadmap.git
cd algorithms-data-structures-roadmap
```

Then open `index.html` in any browser. That's the whole setup.

## Tech

Plain HTML, CSS and JavaScript in a single file. No frameworks, no bundler, no CDN, no external fonts. Diagrams are hand-written and script-generated SVG; theming is done with CSS custom properties, which is also how the figures stay readable in both light and dark mode.

The file is self-contained on purpose: a study guide you cannot open during a power cut or without Wi-Fi is not much of a study guide.

## Sources and attribution

Built from transcripts of the recorded lectures, the course notes (Units 01–10, Dr. Oscar Bruno) and past exams.

**That source material is deliberately not included in this repository.** It is not mine to publish, and the transcripts contain the voices of teaching staff and fellow students. What is published here is the guide itself, which is my own work based on those contents.

If anything here contradicts what your instructor says, go with your instructor.

## Contributing

Found an error, a typo, or an explanation that doesn't hold up? Open an issue. Corrections to the technical content are especially welcome — this is study material, and a wrong explanation is worse than no explanation.

## License

The guide is shared for study purposes under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/): use it, adapt it and share it freely, with attribution and non-commercially. The underlying course material belongs to its authors.

---

<div align="center">
<sub>Made while studying for this exam. If it helps you, leave a star.</sub>
</div>
