# 🐍 Python Practice: Core Language, Data Tooling & Applied Security

[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458.svg)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Array%20Computing-013243.svg)](https://numpy.org/)
[![CUDA](https://img.shields.io/badge/CUDA-GPU%20Computing-76B900.svg)](https://developer.nvidia.com/cuda-toolkit)
[![MCP](https://img.shields.io/badge/MCP-Model%20Context%20Protocol-5A45FF.svg)](https://modelcontextprotocol.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> A working notebook of core Python engineering, applied data tooling (Pandas/NumPy), GPU computing fundamentals (CUDA), the Model Context Protocol (MCP), and offensive/defensive security — spanning quick reference notes, curated course material (CampusX), and a personal library of security and ML-adjacent literature.

---

## 📌 Table of Contents

- [🔬 Overview](#-overview)
- [🗂️ Directory Blueprint](#️-directory-blueprint)
- [🐍 Python Core (`Python/`)](#-python-core-python)
- [📊 Pandas & NumPy (`Pandas/`)](#-pandas--numpy-pandas)
- [🎓 CampusX Curriculum (`CampusX/`)](#-campusx-curriculum-campusx)
- [🛡️ Security (`Security/`)](#️-security-security)
- [⚡ CUDA (`Cuda/`)](#-cuda-cuda)
- [🔌 MCP (`MCP/`)](#-mcp-mcp)
- [⚙️ Setup](#️-setup)
- [👤 Author](#-author)

---

## 🔬 Overview

This repository collects the practice work, handwritten-turned-digital notes, and reference material behind day-to-day Python engineering — not tied to a single project. It's organized by topic rather than chronology:

1. **Language fundamentals** — abstract classes, string formatting, and other core-Python idioms worth keeping as quick reference.
2. **Data tooling** — Pandas/NumPy operations with worked examples and diagrams (merge/join, groupby, concat, split-apply-combine).
3. **Structured curriculum** — the CampusX ML/DL/NLP/PyTorch/FastAPI/LangChain course PDFs, kept as a self-contained study set.
4. **Applied security** — an OWASP Top 10 for LLMs technical deep dive (written from scratch), plus a small library of classic infosec/bug-bounty references.
5. **Systems-adjacent topics** — CUDA GPU programming (NPTEL course) and MCP (Model Context Protocol) for tool-augmented LLM apps.

---

## 🗂️ Directory Blueprint

```
pythonpractice/
├── Python/                                   # Core language notes & references
│   ├── ABC.md                                # Abstract classes & methods (the `abc` module)
│   ├── StringFormatting.md                   # %-formatting → .format() → f-strings, compared
│   └── LearnPython3theHardWay.pdf            # Reference book
│
├── Pandas/                                   # Data manipulation notes, diagrams & sample datasets
│   ├── numpy_arrays.md                       # NumPy array creation/manipulation functions, explained
│   ├── df_groupby_city.png                   # groupby() mechanics diagram
│   ├── split_apply_combine.png               # Split-apply-combine pattern diagram
│   ├── pd_concat.png                         # concat() behavior diagram
│   ├── pf_merge_join.png                     # merge/join semantics diagram
│   ├── nyc_weather.csv, weather_data.csv     # Sample datasets for the exercises above
│
├── CampusX/                                  # CampusX curriculum PDFs (ML/DL/NLP/tooling)
│   ├── 100daysOfML.pdf, 100daysOfDeepLearning-Part-1.pdf, ... Part-2.pdf # Course slide decks
│   ├── DSMP 1 Notes - Part 1.pdf, ... Part 2.pdf     # Data Science Mentorship Program notes
│   ├── Deep Learning Curriculum.pdf, DL Roadmap.pdf  # Curated DL learning paths
│   ├── Deep Learning Resources.pdf                   # Supplementary reading list
│   ├── ML.pdf, NLP.pdf, PyTorch.pdf, FastAPI.pdf      # Topic-specific course material
│   ├── LangChain.pdf                         # LLM app framework notes
│   └── movies.csv                            # Sample dataset used in the exercises
│
├── Security/                                 # Applied security notes & reference library
│   ├── OWASP_LLM_Top_10_Technical_Guide.md   # Hand-written technical deep dive: LLM01–LLM10 attacks & mitigations
│   ├── OWASP LLM.pdf                         # Source OWASP Top 10 for LLM Applications reference
│   ├── mqst-bugbounty-recon-freebie.pdf      # Bug bounty reconnaissance cheat sheet
│   └── Books/                                # Classic infosec reference library
│       ├── Hacking- The Art of Exploitation (2nd ed.) - Erickson.pdf
│       ├── Network Forensics.pdf
│       └── Security Engineering.pdf
│
├── Cuda/                                     # GPU computing fundamentals
│   └── CUDA NPTEL.pdf                        # NPTEL CUDA programming course material
│
└── MCP/                                      # Model Context Protocol
    └── finalmcp.pdf                          # MCP notes — tool-augmented LLM application design
```

---

## 🐍 Python Core (`Python/`)

- **[`ABC.md`](./Python/ABC.md)** — Abstract classes and abstract methods via Python's `abc` module: why they exist, how `@abstractmethod` enforces subclass contracts, and when to reach for them over duck typing.
- **[`StringFormatting.md`](./Python/StringFormatting.md)** — The four generations of Python string formatting (`%`-style, `.format()`, f-strings, and template strings), compared with runnable examples.
- **`LearnPython3theHardWay.pdf`** — Reference textbook kept for offline study.

---

## 📊 Pandas & NumPy (`Pandas/`)

Notes and diagrams built while working through data manipulation fundamentals:

- **[`numpy_arrays.md`](./Pandas/numpy_arrays.md)** — A function-by-function walkthrough of core NumPy array operations (creation, reshaping, indexing) with purpose, syntax, and internal behavior.
- **Diagrams** — Visual explanations of `groupby()`, the split-apply-combine pattern, `concat()`, and merge/join semantics, paired with `nyc_weather.csv` and `weather_data.csv` as working datasets.

---

## 🎓 CampusX Curriculum (`CampusX/`)

A self-contained set of course PDFs from the CampusX Data Science Mentorship Program and related tracks — 100 Days of ML, 100 Days of Deep Learning (Parts 1 & 2), DSMP notes (Parts 1 & 2), and focused decks on ML, NLP, PyTorch, FastAPI, and LangChain — kept as an offline curriculum reference, with `movies.csv` as the accompanying exercise dataset.

---

## 🛡️ Security (`Security/`)

- **[`OWASP_LLM_Top_10_Technical_Guide.md`](./Security/OWASP_LLM_Top_10_Technical_Guide.md)** — An original technical deep dive into the OWASP Top 10 for LLM Applications, covering each vulnerability class (prompt injection, insecure output handling, training data poisoning, supply-chain risk, and more) with problem statements, attacker profiles, technical weaknesses, and mitigations.
- **`OWASP LLM.pdf`** — The underlying OWASP reference document.
- **`mqst-bugbounty-recon-freebie.pdf`** — A condensed bug bounty reconnaissance methodology cheat sheet.
- **`Books/`** — A small classic-infosec library: *Hacking: The Art of Exploitation*, *Network Forensics*, and *Security Engineering* (Ross Anderson).

---

## ⚡ CUDA (`Cuda/`)

`CUDA NPTEL.pdf` — Coursework on CUDA GPU programming fundamentals (memory hierarchy, kernels, parallel execution model), relevant background for understanding how LLM training/inference is accelerated on GPUs.

---

## 🔌 MCP (`MCP/`)

`finalmcp.pdf` — Notes on the Model Context Protocol: how it standardizes tool/resource exposure to LLM applications, and how it fits into building tool-augmented agents without ad-hoc integrations.

---

## ⚙️ Setup

```bash
git clone https://github.com/AvrodeepPal/pythonpractice.git
cd pythonpractice
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install pandas numpy jupyter
```

Most content here is reference material (Markdown notes and PDFs) rather than runnable pipelines — no heavy dependencies required beyond Pandas/NumPy for the notebook-adjacent exercises.

---

## 👤 Author

**Avrodeep Pal**
- GitHub: [@AvrodeepPal](https://github.com/AvrodeepPal)
- Collaboration: Open issues, discussions, or pull requests are warmly welcomed!

⭐ *If you find this repository useful, feel free to star it.*
