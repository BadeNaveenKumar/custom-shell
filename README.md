# 🐚 Custom Shell in C++

## 📘 Project Overview
This project was developed as part of the **Capstone Project (Assignment 2)** for the **Linux Operating System** course.  
It is a **console-based custom shell implemented in C++**, designed to mimic basic Bash functionality such as executing commands, managing processes, handling redirection, and piping.

---

## 🎯 Objectives
- Execute Linux commands directly from the shell.  
- Manage foreground and background processes.  
- Support input/output redirection (`>`, `>>`, `<`).  
- Handle simple piping (`|`).  
- Implement built-in commands: `cd`, `jobs`, `exit`.  
- Gracefully handle process signals.

---

## ⚙️ Features
✅ Run standard commands (`ls`, `pwd`, `date`, `echo`, etc.)  
✅ Manage background jobs using `&` and `jobs`  
✅ Input/output redirection  
✅ Piping between two commands  
✅ Built-in commands (`cd`, `exit`, `jobs`)  
✅ Colored prompt displaying current directory  
✅ Signal handling for background completion  

---

## 🧠 System Calls Used
| Function | Purpose |
|-----------|----------|
| `fork()` | Create new process |
| `execvp()` / `execv()` | Execute program |
| `waitpid()` | Wait for process |
| `open()`, `dup2()`, `close()` | File I/O redirection |
| `pipe()` | Command piping |
| `signal()` | Handle SIGCHLD for background processes |

---

## 🧱 Project Structure
custom_shell/
├── main.cpp
├── Makefile
├── README.md
└── screenshots/
├── compile_success.png
├── run_demo.png
├── cd_navigation.png
├── background_process.png
├── redirection_piping.png


---

## 🚀 How to Compile and Run

### Using G++
```bash
g++ main.cpp -o myshell
./myshell

## Using Makefile
make
make run


