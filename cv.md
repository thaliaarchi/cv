# Thalia Archibald

<thalia@archibald.dev> · [github.com/thaliaarchi](https://github.com/thaliaarchi)

## Summary

I am a second-year PhD student researching compiler verification with John
Regehr at the University of Utah. My research interests include program
transformations, compiler IR design, and formal verification. I have built
several compilers, worked professionally on the GraalVM compiler, and am
proficient in many languages including Rust, C, Rocq, and Go.

## Education

- **University of Utah** · Salt Lake City, Utah

  *PhD in Computer Science*, August 2025 – present

  - Researching compiler verification, advised by [John Regehr](https://users.cs.utah.edu/~regehr/).
  - Developing a rewrite framework for the verified [Veir](https://github.com/opencompl/veir)
    compiler, using acyclic e-graphs.
  - Researched scaling [Alive2](https://alive2.llvm.org/ce/), a translation
    validator for LLVM, to verify more complex programs.

- **Brigham Young University** · Provo, Utah

  *Bachelor of Science in Computer Science*, September 2017 – June 2023

  *Minor in German*

  - Studied programming language theory and systems software, advised by
    [Kimball Germane](https://kimball.germane.net/).
  - Teaching assistant for graduate programming language seminar, theorem
    proving, and discrete mathematics.
  - Achieved CEFR C1 advanced proficiency in German.
  - Leadership role in Cougar Pride Center, advocating for LGBTQ+ students and
    coordinating events.

## Professional Experience

- **Oracle Labs** · Zürich, Switzerland \
  *Research Intern*, July – November 2021

  - Implemented a loop optimization in the GraalVM compiler that improves
    garbage collection performance.
  - This strip mining optimization transforms long-running loops into nested
    loops and moves expensive operations like garbage collection safepoints out
    of the hot inner loop.
  - Unblocked further optimizations, such as vectorization, to combine for large
    speed-ups.

- **GrammaTech** · Remote \
  *Software Engineering Intern*, April – August 2020

  - Built C/C++ static analyses for CodeSonar to enforce configurable naming
    conventions and flag usage of function-like macros.
  - Identified cross-compiler differences and undefined behavior, and tested
    MISRA and C++ standards compliance.
  - Effectively came up to speed in their 30-million-line codebase.

- **6 Degrees Health** · Portland, Oregon \
  *Software Developer*, May – August 2019 \
  *Software Development Intern*, May – August 2018

  - Redesigned from scratch the MediVI healthcare analytics platform for price
    transparency. MediVi was used in every sales call, establishing the
    company's technology-centric reputation, and became the industry archetype.
  - Developed critical features for their claims-management system in
    TypeScript/React and Go.
  - Trained 3 developers and mentored projects.

## Projects

- **Open source**
  - Contributor to the Rust standard library (60 PRs), jq (4 PRs), and Git (1
    patch series).
- **Compiler infrastructure**
  - Implemented various intermediate representations: sea of nodes [[lazy-wspace](https://github.com/thaliaarchi/lazy-wspace)],
    e-graphs [[micro-egg](https://github.com/thaliaarchi/micro-egg)], and static
    single-assignment form [[Nebula](https://github.com/thaliaarchi/nebula)].
  - Implemented loop recurrence recognition and quasi-invariant loop peeling,
    which optimize cases missed by LLVM
    [[bfrs](https://github.com/thaliaarchi/bfrs)].
  - Developed parser with dynamically extensible syntax and error recovery
    [[omniwsa](https://github.com/thaliaarchi/omniwsa)].
  - Developed LLVM IR front-end [[Nebula](https://github.com/thaliaarchi/nebula)].
- **Formal verification**
  - Formalized small compilers in Rocq, proved transformations, and used
    CompCert libraries [[bfcoq](https://github.com/thaliaarchi/bfcoq), [wscoq](https://github.com/thaliaarchi/wscoq)].
  - Reversed MT19937 pseudorandom number generator through cryptanalysis of
    bitwise operations and solved for seeds with Z3 [[Mersenne Untwist](https://github.com/thaliaarchi/mersenne-untwist)].
  - Developed solver engine using binary decision diagrams with bit blasting
    [[bdd-rust](https://github.com/thaliaarchi/bdd-rust)].
- **DevOps**
  - Maintained index of 371 interpreters, compilers, and assemblers with each
    built using Docker [[The Whitespace Corpus](https://github.com/wspace/corpus)].

Projects available at [github.com/thaliaarchi](https://github.com/thaliaarchi).

## Presentations

- **UNIX V4: History and Recovery** / **UNIX V4 and the Utah Teapot**
  - *Computer Graphics Seminar* ·
    University of Utah, 8 September 2026
  - *[Low Resource Computing](https://lrc.cs.dartmouth.edu)* ·
    Dartmouth College, 17–19 August 2026
  - *[SIGGRAPH](https://dl.acm.org/doi/10.1145/3799885.3816010)* ·
    Los Angeles, CA, 23 July 2026
  - *[Languages, Systems, and Data Seminar](https://lsd.ucsc.edu/lsd-seminar/2026sp/#may-22)* ·
    UC Santa Cruz, 22 May 2026
  - *[Vintage Computer Festival Pacific Northwest](https://vcfpnw.org)* ·
    Tukwilla, WA, 2 May 2026
  - *[GradSAC](https://discuss.systems/@thalia/116281783388964930)* ·
    University of Utah, 26 March 2026

  Talk on our recovery of UNIX V4 from a 1974 magnetic tape, the early history
  of this influential operating system, and this artifact’s connection to
  foundational computer graphics research at the University of Utah.
  Demonstrated period software development with UNIX and a printing terminal.
