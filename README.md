<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Python%20Compiler&fontSize=50&fontColor=fff&animation=fadeIn&desc=From%20Source%20Code%20to%20Stack%20Machine%20%7C%20Educational%20Compiler&descSize=16&descAlignY=65"/>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-3776AB?logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/LL(1)%20Parser-0066FF"/>
  <img src="https://img.shields.io/badge/AST-IR%20Pipeline-FF6F00"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow"/>
</p>

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-compilation-pipeline">Pipeline</a> •
  <a href="#-usage">Usage</a> •
  <a href="#-features">Features</a> •
  <a href="#-documentation">Docs</a>
</p>

---

## 🎯 Overview

A complete multi-stage compiler built from scratch in Python. Transforms source code through lexical analysis, syntactic parsing (LL(1)), semantic analysis, intermediate representation generation, and execution on a custom stack machine.

> 📚 Educational project demonstrating the full compilation pipeline — from raw text to executable instructions.

---

## 🔧 Compilation Pipeline

```
Source Code
    │
    ▼
┌─────────────────────┐
│  ① Lexer (Scanner)  │  Tokenizes source → [Token, Token, ...]
└─────────┬───────────┘
          ▼
┌─────────────────────┐
│  ② Parser (LL(1))   │  Builds AST from token stream
└─────────┬───────────┘
          ▼
┌─────────────────────┐
│  ③ Semantic         │  Type checking, scope resolution,
│     Analyzer        │  symbol table validation
└─────────┬───────────┘
          ▼
┌─────────────────────┐
│  ④ IR Generator     │  Intermediate Representation (3-address code)
└─────────┬───────────┘
          ▼
┌─────────────────────┐
│  ⑤ Stack Machine    │  Executes IR on custom virtual machine
└─────────────────────┘
          │
          ▼
      Output
```

---

## 🚀 Usage

```bash
# Run a .gox source file
python main.py examples/mandelplot.gox

# Or use individual stages
python Lexer.py source.gox      # Stage 1: Tokenization
python Parser.py source.gox     # Stage 2: AST Generation
python SemanticAnalyzer.py ...   # Stage 3: Semantic Check
python IRCodeGenerator.py ...    # Stage 4: IR Generation
python StackMachine.py ...       # Stage 5: Execution
```

### Language Features

```
// Variable declarations
var x = 10;
var name = "hello";

// Control flow
if (x >= 5) {
    print(x);
} else {
    print("too small");
}

// Loops
while (x > 0) {
    x = x - 1;
}

// Functions
function fibonacci(n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}
```

---

## ✨ Features

| Stage | Implementation | Status |
|:------|:---------------|:------:|
| **Lexer** | Regex-based tokenizer, keyword recognition, error handling | ✅ Complete |
| **Parser** | LL(1) recursive descent, AST node construction | ✅ Complete |
| **Semantic Analyzer** | Symbol table, type checking, scope management | ✅ Complete |
| **IR Generator** | Three-address code, intermediate representation | ✅ Complete |
| **Stack Machine** | Custom VM, instruction execution, memory management | ✅ Complete |
| **Optimizer** | Constant folding, dead code elimination | ✅ Complete |

### Supported Token Types
| Category | Examples |
|:---------|:---------|
| **Keywords** | `var`, `if`, `else`, `while`, `function`, `return`, `print` |
| **Operators** | `+`, `-`, `*`, `/`, `<=`, `>=`, `==`, `!=`, `=` |
| **Literals** | Integers, floats, strings, booleans |
| **Comments** | Single-line (`//`) and multi-line (`/* */`) |

---

## 📂 Project Structure

```
python-compiler/
├── Lexer.py              # Stage 1: Tokenization
├── Parser.py             # Stage 2: AST Construction
├── SemanticAnalyzer.py   # Stage 3: Type & Scope Checking
├── IRCodeGenerator.py    # Stage 4: Intermediate Representation
├── StackMachine.py       # Stage 5: Virtual Machine Execution
├── Nodes_AST.py          # AST node definitions
├── SymbolTable.py        # Symbol table implementation
├── Error.py              # Error handling framework
├── Types.py              # Type system definitions
├── main.py               # Entry point
├── examples/
│   └── mandelplot.gox    # Example source: Mandelbrot plotter
└── Documentation/        # Full documentation site
    ├── index.html
    ├── Markdown/         # Detailed docs for each stage
    └── src/              # Documented source code
```

---

## 📚 Documentation

A full documentation site is available in the `Documentation/` directory:
- **Lexer**: Token specification, regex patterns, error handling
- **Parser**: Grammar rules, AST node types, LL(1) parsing
- **Semantic Analyzer**: Symbol table, type checking, scope rules
- **IR Generator**: Three-address code, instruction set
- **Stack Machine**: VM architecture, instruction execution

Open `Documentation/index.html` in your browser to explore.

---

## 🧪 Evolution

The compiler evolved through 4 major iterations:

| Version | Improvements |
|:--------|:-------------|
| **v1** | Basic lexer + parser, simple expression evaluation |
| **v2** | Full AST, error handling, symbol table |
| **v3** | Semantic analysis, scope management, type system |
| **v4 (Final)** | IR generation, stack machine, optimizer, doc site |

---

## 📜 License

MIT — See [LICENSE](LICENSE) for details.

---

<p align="center">
  <i>Academic project — Compilers course, UTP Colombia</i>
</p>

<div align="center">
  <a href="https://github.com/SCP-00">SCP-00</a> •
  <a href="https://linkedin.com/in/buendia001">LinkedIn</a>
</div>
