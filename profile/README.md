## Welcome, friends! 👋

We are a distributed team of researchers and engineers 🙋‍.

All of us are crazy about mathematics and programming. We love taking part in software testing [competitions](https://ieeexplore.ieee.org/document/9810769) and describe our achievements in [research articles](https://www.utbot.org/research).

The main project we share is our flagship product — [UnitTestBot](https://www.utbot.org/) for Java/Kotlin, C/C++, 
Python, JavaScript, and Go.

To be in touch with the high-end science, we collaborate with the top-rated universities. As a part of the intercollegiate team, we develop root technologies to empower UnitTestBot as well as the whole lineup of other software products. Here are some of them:

### 🤓 SAT solving technology

SAT solver is a computer program asking whether the variables of a given Boolean formula can be consistently 
replaced by _True_ or _False_ in such a way that the formula evaluates to _True_. SAT solvers are frequently used as the “engine” for the program verification applications.
- [KoSAT](https://github.com/UnitTestBot/kosat) is a pure Kotlin CDCL SAT solver based on MiniSat core. It solves Boolean satisfiability problems given in DIMACS format and supports incremental solving.
- We also investigate [broader theoretical questions](https://www.utbot.org/research) related to SAT solving, e.g. evaluating the computational hardness of a given SAT problem.

### 🧐 SMT solving technology

Satisfiability modulo theories (SMT) field of research relates to determining whether a logic formula is satisfiable.

[KSMT](https://github.com/UnitTestBot/ksmt) is the Java/Kotlin facade for various SMT solvers. For now, it supports 
Z3 and Bitwuzla SAT solvers.

### 😎 Symbolic execution

With SAT and SMT solvers, we develop symbolic execution technology to provide our precise code analysis and 
automated test generation tools with the effective engines. We have three main solutions in this research area.

- [UnitTestBot Java](https://github.com/UnitTestBot/UTBotJava) has its own dynamic symbolic execution engine that has already shown excellent results at [SBST competitions](https://ieeexplore.ieee.org/document/9810769).
- Our custom patch for KLEE is the core of [UnitTestBot C/C++](https://github.com/UnitTestBot/UTBotCpp). KLEE is a symbolic virtual machine built on top of the LLVM compiler infrastructure. 
We [contribute to KLEE](https://github.com/UnitTestBot/klee) by implementing patches that enhance the engine’s code 
  coverage and speed. We offered _lazy initialization improvements_ and committed the _undefined behavior detection patch_ as well as the _patch for inline assembly support_ to the main KLEE branch.
We converted KLEE into the _bidirectional property-directed symbolic execution_ engine. Moreover, the patched KLEE engine is able to automatically deduce method summaries.
- We also plan to support .NET infrastructure via [V#](https://github.com/VSharp-team/VSharp) — the symbolic execution engine performing completely automated test generation for .NET assemblies.

Symbolic execution is the main focus of our interest, so we conducted a [series of research](https://www.utbot.org/research) related to both applied and fundamental problems in this field.

### 🤪 Fuzzing

While working on a UnitTestBot product lineup, we develop [fuzzing and dynamic program analysis techniques](https://github.com/UnitTestBot/UTBotJava/tree/pelevin/UnitTestBot_Family_Fuzzer_Platform/utbot-fuzzers) suitable for all supported languages: Java/Kotlin, C/C++, Python. JavaScript, and Go.


### 🙂 Program analysis
UnitTestBot with its symbolic execution engine and fuzzing techniques is the [ready-to-use](https://github.com/UnitTestBot/UTBotJava/wiki/Static-code-analysis-with-UTBotJava-action) tool for [code analysis](https://github.com/UnitTestBot/UTBotCpp/wiki/CodeAnalyzer).  In addition to this end-to-end solution, we implement a basic framework for developing custom static code analyzers.

[Java Compilation Database (JacoDB)](https://github.com/UnitTestBot/jacodb) was inspired by the [Soot](https://github.com/soot-oss/soot) framework for analyzing and transforming Java code.

JacoDB is a pure Java database that stores information about the compiled Java bytecode — classes, hierarchies, 
annotations, methods, fields, and their usages. With JacoDB, it is possible to analyze bytecode located outside the 
JVM process. It allows UnitTestBot to support the newest JDKs and to reuse data between restarts.

### 🙃 Program synthesis

We investigate approaches to synthesizing code for solving practical problems.
For example, UnitTestBot is able to [generate human-readable test method bodies](https://github.com/UnitTestBot/UTBotJava/pull/1030) based on public API rather than Reflection.

We also develop the **genui** project — a tool for automatic UI generation. In 
our research, we [elaborate](https://icfp22.sigplan.org/details/minikanren-2022-papers/3/On-a-Declarative-Guideline-Directed-UI-Layout-Synthesis) ways to automatically 
arrange the elements of a user interface in accordance with the specified design guidelines. The next step is to 
synthesize the code that is capable of implementing this layout.

## Stay tuned 🧙

Though all these things may sound nerdy, we believe we develop useful tools for real-life programmers. We try to 
make UnitTestBot effective and user-friendly — so that we are happy with it when we use it ourselves.

Feel free to join us in developing UnitTestBot! ✌
