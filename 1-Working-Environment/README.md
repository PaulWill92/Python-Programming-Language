# Python Environment Guide (mise + uv)

This project uses:

- **mise** → manages Python versions  
- **uv** → manages virtual environments and dependencies  

Think:
mise = *which Python*  
uv = *what’s inside the Python*

---

## Install tools (once per machine)

```bash
brew install mise
brew install uv
```

Add `mise` to your shell (zsh):

```bash
echo 'eval "$(mise activate zsh)"' >> ~/.zshrc
```

Restart terminal.

---

Check Versions:

```bash
mise --version
uv --version
```

---

## Starting a New Project

1. Select Python version:

```bash
mise use python@3.12
```

This creates .mise.toml.

Anyone entering this folder will automatically use this python version.

---

1. Initialize project metadata

```bash
uv init
```

creates `pyproject.toml`

---

1. Install dependencies

```bash
uv add pandas streamlit
```

Creates:

```bash
uv.lock
.venv/
```

1. Activate the environment (for manual dev)

```bash
source .venv/bin/activate
```

Leave it later with:

```bash
deactivate
```

---

1. Run code

If activated:

```bash
python app.py
```

Without activating:

```bash
uv run python app.py
```

## Daily Usage

Add a package

```bash
uv add requests
```

Remove a package

```bash
uv remove requests
```

Upgrade dependencies

```bash
uv lock --upgrade
```

Rebuilding the environment (on a new machine)

```bash
mise install
uv sync
```

Done
---

## Git ignore for this process

```gitignore
# ======================================================
# Python
# ======================================================
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
build/
dist/
downloads/
eggs/
.eggs/
lib/
lib64/
parts/
sdist/
var/
wheels/
*.egg-info/
.installed.cfg
*.egg
MANIFEST

# Virtual environments
.venv/
venv/
env/

# ======================================================
# uv
# ======================================================
# (we KEEP uv.lock in git for reproducibility)

# ======================================================
# mise
# ======================================================
# (we KEEP .mise.toml in git)

# ======================================================
# IDE / Editor
# ======================================================
.vscode/
.idea/
*.swp
*.swo

# ======================================================
# Jupyter / Notebooks
# ======================================================
.ipynb_checkpoints/

# ======================================================
# Logs
# ======================================================
*.log

# ======================================================
# OS files
# ======================================================
.DS_Store
Thumbs.db

# ======================================================
# Environment / secrets
# ======================================================
.env
.env.*
*.env

# ======================================================
# Data (adjust depending on project)
# ======================================================
data/
outputs/
artifacts/
tmp/
.cache/

# ======================================================
# Testing / coverage
# ======================================================
.coverage
htmlcov/
.pytest_cache/
.mypy_cache/
.ruff_cache/

# ======================================================
# Streamlit
# ======================================================
.streamlit/secrets.toml
```

Always commit:

```bash
.mise.toml
pyproject.toml
uv.lock
```

Never commit:

```bash
.venv/
data/
secrets
```

## Recommended Python Project Layout

```markdown
my-project/
│
├── pyproject.toml
├── uv.lock
├── .mise.toml
├── README.md
├── .gitignore
│
├── src/
│   └── my_project/
│       ├── __init__.py
│       ├── config.py
│       ├── main.py
│       │
│       ├── data/
│       │   ├── loaders.py
│       │   └── transforms.py
│       │
│       ├── services/
│       │   ├── scraper.py
│       │   └── api.py
│       │
│       ├── models/
│       │   └── churn.py
│       │
│       └── utils/
│           └── helpers.py
│
├── scripts/
│   └── run_scrape.py
│
├── tests/
│   └── test_scraper.py
│
├── notebooks/
│
├── data/          # ignored by git
├── outputs/       # ignored by git
└── artifacts/     # ignored by git
```
