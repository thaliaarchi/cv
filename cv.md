# Thalia Archibald

<thalia@archibald.dev> · [github.com/thaliaarchi](https://github.com/thaliaarchi)

## Summary

I am applying to PhD programs in programming languages and systems software.

In particular, program transformation and analysis interest me, including
compiler mid-end design, rewrite rules, and verifying correctness. I have built
multiple compilers and worked professionally on the GraalVM compiler. I am
effective with many programming languages, including Rust, Coq, Go, and C.

## Education

- **Brigham Young University** · Provo, Utah

  *Bachelor of Science in Computer Science*, September 2017 – June 2023

  *Minor in German*

  - Primarily studied in programming languages and systems software, mentored by
    [Kimball Germane](https://kimball.germane.net/).
  - Teaching assistant for CS 630 Programming Language System Models
    (graduate-level), CS 430 Software Foundations (formalized software in Coq),
    CS 236 Discrete Mathematics (C++), and CS 235 Data Structures (C++).
  - Achieved CEFR C1 “advanced” level proficiency in German.
  - Actively volunteered in the leadership of Cougar Pride Center, coordinating
    events and advocating for rights for queer students.
  - Won honorable mention at the 2023 YHack for my compiler.

## Presentations

- **[Dependent Types: The Calculus of Constructions](https://web.archive.org/web/20230528061056/https://faculty.cs.byu.edu/~kimball/630/dependent-types.html)**,
  7 and 9 March 2023

  Introduction to dependent types in Coq, including demonstrations of a
  [strongly typed `printf`](https://github.com/thaliaarchi/pl-papers/blob/main/coc/printf.v)
  in four styles and a [vector with dependent length](https://github.com/thaliaarchi/pl-papers/blob/main/coc/vec.v).

- **[Collapsing Towers of Interpreters](https://github.com/thaliaarchi/pl-papers/tree/main/cti)**,
  24 and 26 January 2023

  Demonstration of four implementations by me of the languages in “Collapsing
  Towers of Interpreters” (Amin and Rompf, 2018) in Coq and Rust, and discussion
  of partial evaluation and trusting trust (Thompson, 1984).

- **A Brief History of Software Documentation**, 4 October 2022

  Tour of software documentation via comments in the Apollo Guidance Computer
  source, literate programming in TeX, and documentation generation in Rust.

- **[Incremental Computation with Adapton](https://github.com/thaliaarchi/notes/tree/main/logic/adapton)**,
  19 July 2022

  Review of demand-driven incremental computation with Adapton (Hammer et al.,
  2014) and minimal versions, miniAdapton and microAdapton (Fisher et al.,
  2016).

- **[Futamura Projections and Partial Evaluation](https://github.com/thaliaarchi/notes/blob/main/topics/futamura.md)**,
  31 March 2022

  Introduction to partial evaluation of compilers (Futamura, 1971) and live
  coding, applying the first Futamura projection to a simple language.

- **[Architecture of LLVM and tutorial](https://github.com/thaliaarchi/notes/blob/main/compilers/llvm/presentation_outline.md)**,
  8 and 10 March 2022

  Overview of the architecture and design of LLVM, including static
  single-assignment form and the tiered architecture, and walkthrough of
  building an LLVM front-end, demonstrating how various constructs are lowered.

## Writing

- **[Coq typeclass resolution is Turing-complete](https://thaliaarchi.github.io/coq-turing-typeclass/)**,
  15 April 2023

  Proof by construction that the typeclass resolver in Coq can perform arbitrary
  computation while searching for instances.

- **Effects of Compiler Intermediate Representation Design on Ergonomics: A
  Literature Review** (unpublished), 8 December 2022

  Comparative analysis of intermediate representations in LLVM, MLIR, GraalVM,
  CompCert, and WebAssembly.

## Professional Experience

- **Oracle Labs** · Zürich, Switzerland

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

- **GrammaTech** · Remote

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

- **Mobius Labs** · Berlin, Germany

  *Software Engineering Intern*, January – March 2020

  Worked as part of a study abroad for my German minor. Developed an interactive
  web app showcasing the startup's computer vision SDK.

- **6 Degrees Health** · Portland, Oregon

  *Software Developer*, May – August 2019

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

- **EndFirst** · Portland, Oregon

  *Web Development Intern*, Summers 2015 and 2016

  Developed front-end web applications in TypeScript/Angular, including a
  document manager and scheduler.

## Projects

I learn by building and enjoy implementing foundational systems software. My
tools of choice are Rust and Coq. All of these projects and others are published
on my GitHub profile, [thaliaarchi](https://github.com/thaliaarchi).

### Compiler infrastructure

Building compiler infrastructure, particularly in the mid-end, to learn compiler
techniques.

- **[lazy-wspace](https://github.com/thaliaarchi/lazy-wspace) and
  [Nebula](https://github.com/thaliaarchi/nebula) compilers**

  Optimizing compilers in Rust and Go with custom-built intermediate
  representations. They have similar goals, but different approaches.

  - Implemented various intermediate representations: sea of nodes like HotSpot
    and Graal (lazy-wspace) and static single-assignment form with basic blocks
    like LLVM (Nebula).
  - Converted a stack-oriented model to registers by abstractly interpreting
    dynamic stack operations and statically detecting underflow.
  - Integrated with LLVM by generating LLVM IR (Nebula).
  - Built an arena-based IR inspired by Cranelift with global value numbering
    (lazy-wspace).
  - Implemented constant folding and many peephole optimizations for arithmetic
    and bitwise operations.

- **[omniwsa](https://github.com/thaliaarchi/omniwsa) assembler**

  A language front-end and code formatter, which unifies many incompatible
  dialects into one interoperable concrete syntax tree. It has excellent error
  recovery and every program parses to a syntax tree.

### Formal verification

- **[Mersenne Untwist](https://github.com/thaliaarchi/mersenne-untwist)**

  A reverse implementation of the MT19937 Mersenne Twister pseudorandom number
  generator, that can recover the seed in some cases, when given the desired
  outputs.

  - Produced a closed-form reverse implementation that is just as fast as
    forwards, through cryptanalysis of the bitwise operations and value
    dependencies.
  - Implemented an abstract version using Z3, which solves for seeds that
    produce the bits you care about.
  - Developed a high-level Rust API for Z3, that is easier to use than the de
    facto bindings and has stricter static types.

- **[bfcoq](https://github.com/thaliaarchi/bfcoq) and [wscoq](https://github.com/thaliaarchi/wscoq)**

  Small compilers formalized in Coq, that progressively transform through levels
  of intermediate languages. Used components from the CompCert compiler.

- **[Recross](https://github.com/thaliaarchi/recross-coq)**

  Verified regular expression engine in Coq, that has intersection. Includes a
  generic interval set and many rewrites with morphisms.

- **[bdd-rust](https://github.com/thaliaarchi/bdd-rust)**

  An efficient library in Rust for binary decision diagrams with bit blasting
  and an ergonomic API.

### Software history

The history of software inspires me, and I archive old software on the side.

- **[The Regexp Museum](https://github.com/thaliaarchi/regexp-museum)**

  Researching the history and evolution of the syntax, semantics, and code in
  regular expression engines.

  - Discovered novel evolutionary relationships, including tracing the
    development of the original Perl regexp a decade earlier through a
    newsreader, an old Emacs, and UNIX `grep` and `ed`.
  - Cataloged around 100 regular expression implementations.
  - Archived and made usable many old, obscure engines whose influence had been
    forgotten.

- **[git-transform-repo](https://github.com/thaliaarchi/git-transform-repo)**

  Library in Rust to manipulate Git repositories efficiently as streams of data
  and metadata.

  - Zero-copy, streamed parser with excellent error reporting. Allocations are
    performed lazily, when parsed values need to be retained.
  - Contributed patches upstream to Git to harden parsing.

- **[The Whitespace Corpus](https://github.com/wspace/corpus)**

  Collected 368 interpreters, compilers, and assemblers for the Whitespace
  programming language, implemented in 41 programming languages, and engineered
  infrastructure to build and run every project automatically with Docker.
