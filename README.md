### Welcome friends ✌

We are a team of researchers and engineers from Saint Petersburg.

We are crazy about mathematics and programming. We love taking part in software testing competitions. We describe our achievements in [research articles](https://www.utbot.org/research). We develop our flagship product — UnitTestBot for Java/Kotlin, C/C++, Python, JavaScript, and Go.
To be in touch with the high-end science we collaborate with the universities:
- Saint Petersburg State University
- HSE University
- ITMO University
- Peter the Great St. Petersburg Polytechnic University
As a part of this intercollegiate team we develop root technologies to empower UnitTestBot as well as the whole lineup of other software products. Here are some of them:

### SAT solving technology

SAT solver is a computer program which asks whether the variables of a given Boolean formula can be consistently replaced by True or False in such a way that the formula evaluates to True. SAT solvers are frequently used as the “engine” for the program verification applications.
[KoSAT](https://github.com/UnitTestBot/kosat) is a pure Kotlin CDCL SAT solver based on MiniSat core. It solves Boolean satisfiability problems given in DIMACS format and supports incremental solving.
We also investigate [broader theoretical questions](https://www.utbot.org/research) related to SAT solving, e.g. evaluating the computational hardness of a given SAT problem.

### SMT solving technology

Satisfiability modulo theories (SMT) field of research relates to determining whether a logic formula is satisfiable.
KSMT is the Java/Kotlin facade for various SMT solvers. For now it supports Z3 and Bitwuzla SAT solvers.

### Symbolic execution

With SAT and SMT solvers we develop symbolic execution technology to provide our precise code analysis and automated test generation tools with the effective engines. For now we have three main solutions in this research area.

- UnitTestBot for Java has its own dynamic symbolic execution engine that has already shown extremely good results at SBST competitions.
- Our custom patch for KLEE is the core of UnitTestBot for C/C++. KLEE is a symbolic virtual machine built on top of the LLVM compiler infrastructure. 
We contribute to KLEE by implementing patches, which enhance the engine’s code coverage and speed. We offered lazy initialization improvements and committed the undefined behavior detection patch and the patch for inline assembly support to the main KLEE branch.
We converted KLEE into the bidirectional property-directed symbolic execution engine. Moreover, the patched KLEE engine is able to automatically deduce method summaries.
- We also plan to support .NET infrastructure via V# — the symbolic execution engine performing completely automated test generation for .NET assemblies.

Symbolic execution is the main focus of our interest, so we conducted a series of research related to both applied and fundamental problems in this field.

### Fuzzing

When working on a UnitTestBot product lineup, we are developing a fuzzing and dynamic program analysis techniques suitable for all supported languages: Java/Kotlin, C/C++, Python. JavaScript, and Go.


### Program analysis
UnitTestBot with its symbolic execution engine and fuzzing techniques is the ready-to-use tool for code analysis.  In addition to this end-to-end solution we implement a basic framework for developing custom static code analyzers.
Java Compilation Database (JCDB) was inspired by the Soot framework for analyzing and transforming Java code.
JCDB is a pure Java database which stores information about the compiled Java bytecode — classes, hierarchies, annotations, methods, fields, and their usages. With JCDB it is possible to analyze bytecode located outside the JVM process. It allows UnitTestBot to support the newest JDKs and to reuse data between restarts.

### Program synthesis

We investigate approaches to synthesizing code for solving practical problems.
For example, UnitTestBot is capable of generating human-readable test method bodies based on public API rather than Reflection.
We also develop the genui project — a tool for automatic UI generation. In our research we elaborate ways to automatically arrange the elements of a user interface in accordance with the specified design guidelines. The next step is to synthesize the code which is capable to implement this layout.


Though all these things may sound nerdy, we believe we develop useful tools for real-life programmers. We try to make UnitTestBot effective and user-friendly — so that we are happy with it when we use it ourselves. And we welcome you to join us in developing UnitTestBot!
Visit our GitHub page and feel free to contribute.
Contact us directly to ask a question, share your ideas or give us feedback — we will be glad to hear from you!
