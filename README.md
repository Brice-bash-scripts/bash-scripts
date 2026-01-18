# 🛠️ Linux Bootstrap Scripts

A personal collection of **Bash utility scripts** used to quickly set up, navigate, and initialize projects when starting work in a Linux / WSL environment.

These scripts live in my `~/scripts` directory and are intended to be:

- lightweight
- fast
- composable
- opinionated (by design)

They encode my **default workflow assumptions** so I don’t have to re-think setup every time.

---

## 📂 Repository Structure

```plaintext
scripts/
├── docs/
│   ├── structure.md        # Explanation of the project structure created
│   └── executable_usage.md  # Instructions for making scripts executable
├── find.sh        # Fast file / directory search helpers
├── intro.sh       # Environment intro / sanity checks (.gitignore)
├── mkconda        # Conda environment creation helper
├── mkvenv         # Python venv creation helper
├── mkml_repo_setup   # Project repository scaffold generator for ML projects
├── mkback_repo_setup   # Project repository scaffold generator for backend projects
├── .gitignore
└── README.md
```

---

## 🎯 Design Philosophy

These scripts are intentionally:

- **Simple** – no heavy dependencies
- **Composable** – each script does one thing well
- **Fast** – optimized for daily use
- **Opinionated** – reflects how *I* work, not generic defaults

They are not meant to replace configuration management tools (Ansible, etc.).
They are meant to **remove friction** from day-to-day development.

---

## 🧰 Script Overview

### `mkrepo_setup`

Creates a **fully structured project repository** with:

- `src/` layout (FastAPI / Python-friendly)
- ML-ready directories (`data/`, `artifacts/`, `notebooks/`)
- Pre-organized `docs/` taxonomy
- `.gitignore` with ML-safe defaults
- `.dockerignore` ready for future containerization
- `.env.example`
- Git-tracked empty directories via `.gitkeep`

This is the script I use most often.

---

### `mkvenv`

Creates a standard Python virtual environment and activates it.

Used when I want:

- lightweight environments
- no Conda overhead
- quick experimentation

---

### `mkconda`

Creates a Conda environment with my preferred defaults.

Used when:

- working on data science / ML projects
- needing compiled dependencies
- isolating heavier environments

---

### `find.sh`

Convenience wrapper for faster file or directory lookup.

Primarily used to:

- locate files in large repos
- avoid repeated `find` command typing

---

### `intro.sh`

Quick environment sanity check / intro script.

Typically used to:

- verify shell configuration
- confirm paths and tooling
- provide a “known good” starting state

---

## 🚀 Typical Workflow

```bash
cd ~/projects
mkrepo_setup my_new_project
cd my_new_project
mkvenv
```

Or for ML-heavy work:

```bash
mkrepo_setup pipeline_risk_model
mkconda
```

From there, I can immediately:

- start coding
- start documenting
- start modeling

No setup ceremony.

---

## 🧠 Why These Scripts Exist

Over time, I found myself repeatedly doing the same things:

- recreating project structures
- forgetting directories
- mis-organizing repos
- re-learning my own conventions

These scripts **encode decisions** so I don’t have to keep making them.

They also make my workflow:

- more reproducible
- easier to teach
- easier to evolve

---

## ⚠️ Notes & Assumptions

- These scripts assume a **Linux / WSL environment**
- They are designed for **interactive use**
- They reflect *my* preferred project structure
- They may evolve as my workflow evolves

This repo is intentionally **not generic**.

---

## 🔮 Future Enhancements (Optional)

- flags for `mkrepo_setup` (`--ml`, `--api`, `--db`)
- dry-run mode
- logging / verbose mode
- optional FastAPI boilerplate generation

---

## 📜 License

Personal use.
Steal ideas freely.
Blame me if something breaks 😄
