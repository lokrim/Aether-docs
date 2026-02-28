---
id: macos-setup
title: macOS Setup
sidebar_position: 1
---

# macOS Set Up

This guide will walk you through setting up your macOS environment for Project Aether.

## 1. Install Homebrew
Homebrew is the package manager for macOS. It makes installing dependencies extremely easy. Open your terminal and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 2. Install Git
Git should come pre-installed on macOS, but it's best to install the latest version via Homebrew:

```bash
brew install git
```

## 3. Install Python
We recommend using Python 3.9 or higher. Install it using Homebrew:

```bash
brew install python
```

## 4. Install Node.js and Yarn
Since our documentation is built with Docusaurus, you will need Node.js and Yarn.

```bash
brew install node
npm install --global yarn
```

## 5. Clone the Repository
Finally, clone the repository to your local machine:

```bash
git clone https://github.com/sfu-akcse/Aether.git
cd Aether
```
