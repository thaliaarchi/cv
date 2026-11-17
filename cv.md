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

The history of software inspires me, and I archive and study influential old
software on the side.

- [UNIX History at Utah](https://github.com/thaliaarchi/unix-history)

  Researching the early use of UNIX at the University of Utah in 1974 to tell
  the story of our [recently found UNIX V4 tape](https://www.theregister.com/2025/11/07/unix_fourth_edition_tape_rediscovered/),
  the only surviving copy of the first public version of this influential
  operating system.

- **[The Regexp Museum](https://github.com/thaliaarchi/regexp-museum)**

  Researching the history and evolution of the syntax, semantics, and code
  across regular expression engines.

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
