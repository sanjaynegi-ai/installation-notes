# Windows Infrastructure Setup for GitHub Copilot + VS Code

---

## 1️⃣ Objective

Prepare a **clean, production-grade Windows development environment** that:

* Runs VS Code with correct configuration
* Uses GitHub Copilot correctly
* Enforces secure coding habits
* Enables future RAG + Agentic system development

By the end, everyone should:

* Have Copilot inline suggestions working
* Have Copilot Chat working
* Be able to refactor safely
* Be able to generate tests using structured prompts
* Be operating inside a disciplined workflow

---

## 2️⃣ Concepts

From **VS Code Configuration** :

Required Extensions:

* GitHub Copilot
* GitHub Copilot Chat
* GitLens
* Error Lens

Required Settings:

* `editor.inlineSuggest.enabled = true`
* `copilot.enableAutoCompletions = true`
* `editor.codeActionsOnSave enabled`

From **GitHub Copilot Best Practices** :

Copilot excels at:

* Boilerplate
* Refactoring without behavior change
* Test generation
* Documentation scaffolding

Security rules:

* Never accept secrets
* Review auth/crypto
* Validate SQL and shell commands

You are not installing a toy.
You are installing a junior engineer that must be supervised.

---

## 3️⃣ Copilot Skill Focus

Everyone must learn immediately:

* Inline completion acceptance vs rejection
* Prompting inside the IDE (structured prompts)
* Reviewing generated code
* Refusing insecure suggestions
* Using Copilot Chat for refactors, not guessing

---

## 4️⃣ Hands-On Tasks (Step-by-Step Setup)

Follow this in order. No skipping.

---

# STEP 1 – Windows System Preparation

### 1.1 Update Windows

* Settings → Windows Update
* Install all pending updates
* Reboot

Why?
Outdated Windows causes terminal, WSL, and extension instability.

---

# STEP 2 – Install Required Infrastructure

### 2.1 Install Git

Download from:
[https://git-scm.com/download/win](https://git-scm.com/download/win)

During install:

* Use Git from command line
* Default line endings
* Enable symbolic links

Verify:

```powershell
git --version
```

---

### 2.2 Install Node.js (IF NOT ALREADY DONE) 

Download:
[https://nodejs.org/](https://nodejs.org/)

Install LTS version.

Verify:

```powershell
node -v
npm -v
```

Why now?
Later phases require embeddings, APIs, agent frameworks.

---

### 2.3 (Recommended) Install Python 3.11+ (go for latest)

Download:
[https://www.python.org/downloads/](https://www.python.org/downloads/)

Check:

```powershell
python --version
pip --version
OR
python -m pip --version
```

You will need this in Phase 3.

---

# STEP 3 – Install Visual Studio Code

Download:
[https://code.visualstudio.com/](https://code.visualstudio.com/)

During installation:

* Add to PATH
* Register as default editor
* Enable “Open with Code” context menu

Verify:

```powershell
code --version
```

---

# STEP 4 – Install Required Extensions (MANDATORY)

Open VS Code → Extensions panel

Install:

1. GitHub Copilot
2. GitHub Copilot Chat
3. GitLens
4. Error Lens

These are required configuration .

---

# STEP 5 – GitHub Authentication

1. Sign into GitHub in browser
2. Open VS Code
3. Click Account → Sign in with GitHub
4. Authorize Copilot

Verify:

* Open a `.js` or `.py` file
* Type a function signature
* Wait for gray inline suggestion

If no suggestion appears:

* Restart VS Code
* Check Copilot status in bottom bar

---

# STEP 6 – Configure VS Code Settings

Open:
File → Preferences → Settings → Open JSON Settings

Add:

```json
...
   "editor.inlineSuggest.enabled": true,
   "github.copilot.enable": {
        "*": true
    },
    "editor.codeActionsOnSave": {
        "source.fixAll": "always"
    },
    "chat.viewSessions.orientation": "stacked"
...
```

These align with required settings .

Restart VS Code.

---

# STEP 7 – Configure Git Properly (provide appropriate values as per your details in Github profile)

In terminal:

```bash
git config --global user.name "Full Name"
git config --global user.email "youremail@gmail.com"
git config --global init.defaultBranch main
```

Verify:

```bash
git config --list
```

---

# STEP 8 – Security Baseline

Before writing code:

You must understand Copilot security rules :

* Never accept hardcoded passwords
* Never accept API keys in code
* Review SQL queries
* Review shell commands
* Review authentication logic




