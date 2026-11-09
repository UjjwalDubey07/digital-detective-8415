# Mission 4: How Programs Run

## Task 4.1 — Create and Run a Python Program

**File created:** `mission-04-programs/hello.py`

**Content of hello.py:**
```python
print("Hello from Python")

Command used to run:
python3 hello.py

Output observed:
Hello from Python

---

Task 4.2 — Compiler vs Interpreter Comparison

┌───────────────────────────────┬──────────────────────────────────────────────────────────────────────────────┬─────────────────────────────────────────────────────────────────────────────────────────┐
│             Point             │                                   Compiler                                   │                                       Interpreter                                       │
├───────────────────────────────┼──────────────────────────────────────────────────────────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────┤
│ When translation / execution  │ Entire source code is translated to machine code before execution            │ Source code is read, translated, and executed line-by-line at runtime.                  │
│ happens                       │ (ahead-of-time).                                                             │                                                                                         │
├───────────────────────────────┼──────────────────────────────────────────────────────────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────┤
│ Typical output                │ Standalone executable binary (e.g., .exe, a.out, .o) that can run            │ No separate executable; the interpreter program runs the source directly.               │
│                               │ independently.                                                               │                                                                                         │
├───────────────────────────────┼──────────────────────────────────────────────────────────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────┤
│ One example                   │ gcc (C/C++), rustc (Rust), javac (Java → bytecode)                           │ python3, node (JavaScript), ruby, bash                                                  │
├───────────────────────────────┼──────────────────────────────────────────────────────────────────────────────┼─────────────────────────────────────────────────────────────────────────────────────────┤
│ One advantage                 │ Fast execution — optimized machine code runs directly on CPU; no translation │ Easier development cycle — no compile step; immediate feedback; portable source runs    │
│                               │  overhead at runtime.                                                        │ anywhere interpreter exists.                                                            │
└───────────────────────────────┴──────────────────────────────────────────────────────────────────────────────┴─────────────────────────────────────────────────────────────────────────────────────────┘

Explanation:
A compiler translates the entire source code into machine code before the program runs, producing a standalone executable that the CPU can execute directly. An interpreter, by contrast, reads the source code line by line and executes it at runtime, without creating a separate binary. This means compiled programs generally run faster because the translation work is done upfront, while interpreted programs offer a faster edit-run-debug cycle since you skip the compilation step. Many modern languages (like Java, Python) blend both: they compile to an intermediate bytecode which is then interpreted or JIT-compiled.

---

Mission 4 Summary & Reflection

- Files created: hello.py
- Commands used: python3 hello.py
- Key concepts: Ahead-of-time compilation vs runtime interpretation, executable vs source execution, trade-offs (speed vs development velocity).
- Challenges & Resolution: ["No issues; Python ran successfully."]
