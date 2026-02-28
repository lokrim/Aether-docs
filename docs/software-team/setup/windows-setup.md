---
id: windows-setup
title: Windows / Linux Setup
sidebar_position: 2
---

# Windows / Linux Set Up

This guide will walk you through setting up your environment for Project Aether on Windows or Linux.

## 1. Install Git

### Windows
Download and install Git from the [official website](https://git-scm.com/download/win). We highly recommend using Git Bash (included in the installation) as your primary terminal.

### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install git
```

## 2. Install Python
We recommend using Python 3.9 or higher.

### Windows
Download the installer from the [official Python website](https://www.python.org/downloads/windows/). 
> **Important:** During installation, ensure you check the box that says **"Add Python to PATH"**.

### Linux (Ubuntu/Debian)
```bash
sudo apt install python3 python3-pip python3-venv
```

## 3. Install Node.js and Yarn
Since our documentation is built with Docusaurus, you will need Node.js and Yarn.

### Windows
Download the installer from the [Node.js website](https://nodejs.org/).
After installation, open your terminal (Git Bash or PowerShell) and run:
```bash
npm install --global yarn
```

### Linux (Ubuntu/Debian)
```bash
# Install Node.js via NVM (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
source ~/.bashrc
nvm install node

# Install Yarn
npm install --global yarn
```

## 4. Clone the Repository
Finally, clone the repository to your local machine:

```bash
git clone https://github.com/sfu-akcse/Aether.git
cd Aether
```
