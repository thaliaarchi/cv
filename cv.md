# Thalia Archibald

<thalia@archibald.dev> · [github.com/thaliaarchi](https://github.com/thaliaarchi)

## Summary

I am a second-year PhD student researching compiler verification with John
Regehr at the University of Utah. My research interests include program
transformations, compiler IR design, and formal verification. I aim to advance
research in composable, verifiable, and scalable compiler infrastructures. I
have built several compilers, worked professionally on the GraalVM compiler, and
am proficient in many languages including Rust, C, Coq, and Go.

## Education

- **University of Utah** · Salt Lake City, Utah

  *PhD in Computer Science*, August 2025 – present

  - Advised by [John Regehr](https://users.cs.utah.edu/~regehr/).
  - Ongoing research to extend [Alive2](https://alive2.llvm.org/ce/), a
    translation validator for LLVM, to reason about loops without unrolling.

- **Brigham Young University** · Provo, Utah

  *Bachelor of Science in Computer Science*, September 2017 – June 2023

  *Minor in German*

  - Studied programming language theory and systems software, mentored by
    [Kimball Germane](https://kimball.germane.net/).
  - Teaching assistant for CS 630 Programming Language System Models
    (graduate-level), CS 430 Software Foundations (formalized software in Coq),
    CS 236 Discrete Mathematics (C++), and CS 235 Data Structures (C++).
  - Achieved CEFR C1 “advanced” proficiency in German.
  - Leadership role in Cougar Pride Center, advocating for queer students and
    coordinating events.
  - Won honorable mention at the 2023 YHack for my compiler.

## Professional Experience

- **Oracle Labs** · Zürich, Switzerland \
  *Research Intern*, July – November 2021

  - Implemented an optimization phase in the core of the GraalVM compiler. It
    performs “strip mining” on long-running loops in Java programs, transforming
    them into nested loops and moving overhead-heavy operations out of the inner
    loop.
  - This reduces the execution cost of safepoint polling for garbage collection
    and improves performance with low-pause-time garbage collectors. It also
    enables further optimizations, such as vectorization, that combine for large
    speed-ups.
  - Became one of 5 people who understands the complex infrastructure for loops
    in Graal.

- **GrammaTech** · Remote \
  *Software Engineering Intern*, April – August 2020

  - Built static analyses for CodeSonar, which enforce naming convention styles
    configurably like Clang and flag usage of function-like macros instead of
    functions in C/C++ code.
  - Implemented a regular expression that expanded to 1100 characters, which
    precisely handles all lexical C++ features before preprocessing.
  - Identified cross-compiler differences and undefined behavior, and tested
    MISRA and C++ standards compliance.
  - Effectively came up to speed in their 30-million-line codebase, despite
    unexpected remote mentorship due to COVID.

- **6 Degrees Health** · Portland, Oregon \
  *Software Developer*, May – August 2019 \
  *Software Development Intern*, May – August 2018

  - Developed the redesigned MediVI healthcare cost analytics platform from
    scratch. At the time there was no comparable tool on the market and MediVI
    has since become the industry archetype. It was pivotal to the success of
    the company: MediVI was used in every sales call, cementing their
    technology-centric reputation in healthcare pricing, and contributed to
    their $85 million valuation. Even as an intern, I had an oversized impact on
    this startup.
  - Developed many features for the in-house healthcare claims-management system
    in TypeScript/React and Go.
  - Trained 3 new developers and mentored projects.

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

  Talk on our recovery of UNIX V4 from a 1974 magnetic tape, the
  early history of this influential operating system, and this
  artifact’s connection to foundational computer graphics research at
  the University of Utah. Some presentations demonstrated period
  software development with a printing terminal.
