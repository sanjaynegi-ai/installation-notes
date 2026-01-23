# Installing n8n on Windows Using NVM

This document provides step-by-step instructions for installing **n8n** on Windows using **NVM (Node Version Manager)**.
Using NVM is recommended because it allows easy management of Node.js versions, which is important for n8n compatibility.

---

## Overview

**n8n** is a workflow automation platform built on Node.js.
To run n8n reliably on Windows, we will:

1. Install **NVM for Windows**
2. Install **Node.js (LTS)** using NVM
3. Install **n8n** globally using npm
4. Run and verify n8n

---

## Prerequisites

* Windows 10 or Windows 11 (64-bit)
* Administrator access
* Internet connection
* Command Prompt or PowerShell

---

## Step 1: Install NVM for Windows

> Note: Windows uses **nvm-windows**, which is different from macOS/Linux NVM.

### 1. Download NVM

* Visit: [https://github.com/coreybutler/nvm-windows/releases](https://github.com/coreybutler/nvm-windows/releases)
* Download the latest **`nvm-setup.exe`**

### 2. Run the Installer

* Double-click `nvm-setup.exe`
* Accept the license agreement
* Keep default installation paths
* Complete the installation

### 3. Verify Installation

Open **Command Prompt** or **PowerShell** and run:

```bash
nvm version
```

If a version number is returned, NVM is installed correctly.

---

## Step 2: Install Node.js Using NVM

n8n works best with a **Node.js LTS** version.

### 1. View Available Node Versions

```bash
nvm list available
```

### 2. Install an LTS Version

```bash
nvm install 20.19.6
```

> Replace `20.19.6` with the latest LTS version if needed.

### 3. Activate the Installed Version

```bash
nvm use 20.19.6
```

### 4. Verify Node.js and npm

```bash
node -v
npm -v
```

Both commands should return version numbers.

---

## Step 3: Install n8n

Install n8n globally using npm:

```bash
npm install -g n8n
```

### Verify Installation

```bash
n8n --version
```

If a version number appears, n8n is installed successfully.

---

## Step 4: Run n8n

Start n8n with the following command:

```bash
n8n
```

By default:

* n8n runs on port **5678**
* URL: `http://localhost:5678`

Open a browser and navigate to:

```
http://localhost:5678
```

---

## Step 5: First-Time Setup

On first launch:

1. Create an admin user / owner account, by filling with appropriate information
2. Fill informaton in subsequent screen(s) ( provide you emailID for *free activation key* for advanced features and follow the instructions )


After setup, the n8n workflow editor will load.

---

## Optional: Set a Custom Data Directory

By default, n8n stores data in the user home directory.
To customize the location:

```bash
setx N8N_USER_FOLDER "C:\n8n"
```

Restart the terminal for the change to take effect.

---

## Useful NVM Commands (Reference)

```bash
nvm list                 # List installed Node versions
nvm list available       # List available Node versions
nvm use <version>        # Switch Node version
nvm uninstall <version> # Remove a Node version
```

---

## Common Issues and Solutions

### `n8n is not recognized as a command`

* Restart the terminal
* Ensure Node is active:

  ```bash
  nvm use 20.19.6
  ```

### Port 5678 Already in Use

Run n8n on a different port:

```bash
set PORT=5679 && n8n
```

### Permission Errors

* Run Command Prompt or PowerShell as **Administrator**
* Ensure Node.js is installed only via NVM

---
