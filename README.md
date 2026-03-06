<div align="center">

# 🐚 Custom Shell in C++

> A fully-featured, Bash-inspired shell built from scratch in C++ — crafted as a Linux OS Capstone Project.

[![Language](https://img.shields.io/badge/Language-C%2B%2B-blue?style=for-the-badge&logo=cplusplus)](https://isocpp.org/)
[![Platform](https://img.shields.io/badge/Platform-Linux-orange?style=for-the-badge&logo=linux)](https://www.linux.org/)
[![Build](https://img.shields.io/badge/Build-Makefile-green?style=for-the-badge&logo=gnu)](https://www.gnu.org/software/make/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)]()

</div>

---

## 📋 Table of Contents

- [📘 Overview](#-overview)
- [🎯 Objectives](#-objectives)
- [⚙️ Features](#️-features)
- [🧠 System Calls Used](#-system-calls-used)
- [🧱 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
- [🖥️ Demo & Screenshots](#️-demo--screenshots)
- [🤝 Contributing](#-contributing)
- [👤 Author](#-author)

---

## 📘 Overview

This project was developed as the **Capstone Project (Assignment 2)** for the **Linux Operating System** course.

It is a **console-based custom shell implemented in C++**, designed to mimic core Bash shell functionality — including command execution, process management, I/O redirection, and piping — all built using low-level Linux system calls.

---

## 🎯 Objectives

| # | Objective |
|---|-----------|
| 1 | Execute standard Linux commands directly from the shell |
| 2 | Manage foreground and background processes |
| 3 | Support input/output redirection (`>`, `>>`, `<`) |
| 4 | Handle command piping (`\|`) |
| 5 | Implement built-in commands: `cd`, `jobs`, `exit` |
| 6 | Gracefully handle UNIX process signals |

---

## ⚙️ Features

```
╔════════════════════════════════════════════════════════════╗
║                   CUSTOM SHELL FEATURES                    ║
╠════════════════════════════════════════════════════════════╣
║  ✅  Run standard commands  (ls, pwd, date, echo, ...)     ║
║  ✅  Background job management  (& operator + jobs)        ║
║  ✅  Input / Output redirection  (>, >>, <)                ║
║  ✅  Command piping  (cmd1 | cmd2)                         ║
║  ✅  Built-in commands  (cd, exit, jobs)                   ║
║  ✅  Colored prompt with current directory                 ║
║  ✅  Signal handling for background process completion     ║
╚════════════════════════════════════════════════════════════╝
```

---

## 🧠 System Calls Used

| System Call | Purpose |
|-------------|---------|
| `fork()` | Spawn a new child process |
| `execvp()` / `execv()` | Execute an external program |
| `waitpid()` | Wait for a specific child process to finish |
| `open()` | Open files for redirection |
| `dup2()` | Redirect file descriptors (stdin/stdout) |
| `close()` | Close unused file descriptors |
| `pipe()` | Create a unidirectional data channel between processes |
| `signal()` | Register handler for `SIGCHLD` (background process cleanup) |

---

## 🧱 Project Structure

```
custom-shell/
│
├── 📄 Main.cpp          # Core shell implementation
├── 🔧 Makefile          # Build automation
├── 📖 README.md         # Project documentation
│
└── 📁 Screen shots/     # Demo screenshots
    ├── 🖼️  compile_success.png
    ├── 🖼️  run_demo.png
    ├── 🖼️  cd_navigation.png
    ├── 🖼️  background_process.png
    └── 🖼️  redirection_piping.png
```

---

## 🚀 Getting Started

### Prerequisites

- **Linux** operating system (Ubuntu, Fedora, Arch, etc.)
- **g++** compiler (GCC 7+ recommended)
- **make** (optional, for Makefile build)

### Option 1 — Compile with G++

```bash
# Clone the repository
git clone https://github.com/BadeNaveenKumar/custom-shell.git
cd custom-shell

# Compile
g++ Main.cpp -o myshell

# Run
./myshell
```

### Option 2 — Build with Makefile

```bash
# Clone the repository
git clone https://github.com/BadeNaveenKumar/custom-shell.git
cd custom-shell

# Build & Run
make
make run

# Clean build artifacts
make clean
```

---

## 🖥️ Demo & Screenshots

### Shell in Action

| Feature | Screenshot |
|---------|------------|
| ✅ Compile Success | `Screen shots/compile_success.png` |
| 🖥️ Shell Running | `Screen shots/run_demo.png` |
| 📁 Directory Navigation (`cd`) | `Screen shots/cd_navigation.png` |
| ⚙️ Background Process (`&`) | `Screen shots/background_process.png` |
| 🔀 Redirection & Piping | `Screen shots/redirection_piping.png` |

---

### Example Usage

```bash
# Run a standard command
myshell> ls -la

# Navigate directories
myshell> cd /home/user/projects

# Pipe commands
myshell> ls -l | grep ".cpp"

# Output redirection
myshell> echo "Hello World" > output.txt

# Append to file
myshell> echo "More text" >> output.txt

# Input redirection
myshell> sort < unsorted.txt

# Run in background
myshell> sleep 10 &

# List background jobs
myshell> jobs

# Exit shell
myshell> exit
```

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add some amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

---

## 👤 Author

<div align="center">

**Naveen Kumar Bade**

[![GitHub](https://img.shields.io/badge/GitHub-BadeNaveenKumar-181717?style=for-the-badge&logo=github)](https://github.com/BadeNaveenKumar)

*Capstone Project — Linux Operating System Course*

</div>

---

<div align="center">

⭐ **If you found this project helpful, please give it a star!** ⭐

Made with ❤️ and C++

</div>


