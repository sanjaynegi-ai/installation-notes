# uv Notes & Common Commands

---

## 🔑 Core Concepts

* **Virtual Environment**: Isolated Python setup for one project
* **`.venv` folder**: Default location for environments
* **Speed**: Much faster installs than traditional tools
* **Modern workflow**: Works well with `pyproject.toml`

---

## 🌱 Virtual Environments with uv

### Create a virtual environment

```bash
uv venv
```

Creates a `.venv` folder in the current directory.

---

### Activate the environment (Windows)

```bash
.venv\Scripts\activate
```

---

### Deactivate environment

```bash
deactivate
```

---

## 📦 Package Management Commands

| Purpose                       | Command                              |
| ----------------------------- | ------------------------------------ |
| Install a package             | `uv pip install package_name`        |
| Install from requirements.txt | `uv pip install -r requirements.txt` |
| Uninstall a package           | `uv pip uninstall package_name`      |
| List installed packages       | `uv pip list`                        |
| Freeze dependencies           | `uv pip freeze`                      |

---

## 📄 Working with pyproject.toml

### Install project dependencies

```bash
uv pip install .
```

---

### Add a dependency (recommended)

```bash
uv add package_name
```

---

## 📌 When to Use uv

`uv` is best for:

* Modern Python development
* Fast dependency installation
* Projects using `pyproject.toml`
* Developers comfortable with the command line

---

## ⚠️ Beginner Notes

* `uv` does **not** install Python
* No graphical interface

---

## 🆚 uv vs Conda (Quick Comparison)

| Feature           | Conda       | uv          |
| ----------------- | ----------- | ----------- |
| Beginner friendly | ✅ Yes       | ⚠️ Moderate |
| Speed             | 😐 Medium   | ⚡ Very fast |
| Bundles Python    | ✅ Yes       | ❌ No        |
| GUI               | ✅ Navigator | ❌ No        |

---

