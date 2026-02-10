# Anaconda Notes & Common Commands

## What is Conda?

Conda is a tool that:

* Installs Python packages
* Creates isolated environments
* Prevents version conflicts between projects

---

## 🔑 Common Conda Commands

| Purpose                 | Command                      |
| ----------------------- | ---------------------------- |
| Check Conda version     | `conda --version`            |
| Update Conda            | `conda update conda`         |
| Check Python version    | `python --version`           |
| List installed packages | `conda list`                 |
| Install a package       | `conda install package_name` |
| Remove a package        | `conda remove package_name`  |

---

# 🌱 Virtual Environments (Very Important)

## Why Environments?

* Keep projects separate
* Avoid library version conflicts
* Safely experiment without breaking other projects

---

## Environment Commands

| Purpose                | Command                                |
| ---------------------- | -------------------------------------- |
| Create environment     | `conda create -n env_name python=3.11` |
| Activate environment   | `conda activate env_name`              |
| Deactivate environment | `conda deactivate`                     |
| List environments      | `conda env list`                       |
| Delete environment     | `conda remove -n env_name --all`       |

---

# 📓 Jupyter Commands

| Purpose                | Command            |
| ---------------------- | ------------------ |
| Start Jupyter Notebook | `jupyter notebook` |
| Start JupyterLab       | `jupyter lab`      |

> These commands open Jupyter in your web browser.

---

# 📌 When to Use Anaconda

Anaconda is best for:

* Beginners learning Python
* Data Science & Machine Learning
* Scientific computing
* University courses
* Projects needing many libraries

---

# ⚠️ Common Beginner Tips

* Always use **Anaconda Prompt**, not Command Prompt
* Create a **new environment for each project**
* Do not mix `pip` and `conda` unless you know why
* If something breaks, environments save you

---

# ✅ Summary

* Anaconda simplifies Python setup
* Conda manages packages and environments
* Jupyter lets you code interactively
* Ideal for students and beginners

---

