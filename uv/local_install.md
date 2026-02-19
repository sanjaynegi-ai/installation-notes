# uv – Beginner Notes ⚡🐍

## What is uv?

**`uv`** is a modern, fast tool for managing **Python packages and virtual environments**. It helps developers install libraries and create environments much faster than traditional tools. `uv` is developed by **Astral**.

Unlike Anaconda, `uv` does **not** bundle Python or libraries. It uses an **existing Python installation** and focuses on speed and modern workflows.

> 💡 Think of `uv` as a fast replacement for `pip + venv`.

---

## Installing uv on Windows

### Prerequisites

* Windows 10 or Windows 11
* Python 3.8 or newer **already installed**
* Internet connection

Check Python:

```bash
python --version
```

---

### Step 1: Install uv

Open **PowerShell** and run:

```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

---

### Step 2: Verify installation

```bash
uv --version
```

If a version number appears, `uv` is installed correctly ✅

---

### Step 3: Update uv (Optional)

```bash
uv self update
```

---

### Important Difference from Anaconda

| Anaconda         | uv                 |
| ---------------- | ------------------ |
| Bundles Python   | Uses system Python |
| GUI included     | Command-line only  |
| Beginner-focused | Developer-focused  |

