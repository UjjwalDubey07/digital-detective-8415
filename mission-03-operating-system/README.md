# Mission 3: Operating System, Processes, Paths & Permissions

## Task 3.1 — Explore Your Operating System

| Information Explored | What it tells you | Your Observation (privacy-safe) |
| :--- | :--- | :--- |
| Operating system / system details | OS name, version, build — identifies the kernel and userland environment | [e.g., macOS 14.6.1 (23G93)] |
| Current account identity | Which user is logged in, their UID/GID — determines file ownership and permissions | [e.g., User: [redacted], UID: 501] |
| Available and used storage | Free/used space on the boot volume — shows capacity for new files | [e.g., 200G free / 500G total] |
| System activity snapshot | Running processes, CPU/memory usage — shows system load and active programs | [150 processes, 5% CPU, 8G/16G RAM used] |

**Commands used:** `sw_vers`, `whoami`, `df -h /`, `ps aux` (or `top -l 1`)

---

## Task 3.2 — Understand Processes

**Commands used:** `ps aux` (or `top` / `htop`)

**Answers:**

1. **What is a process?**
   A process is an instance of a program that is currently executing in memory. It has its own memory space, resources (file descriptors, CPU time), and a unique Process ID (PID).

2. **What does the PID column represent?**
   PID (Process Identifier) is a unique number assigned by the OS to each running process. It allows the kernel and users to reference, signal, or manage a specific process (e.g., `kill 1234`).

3. **Two examples of processes on your computer:**
   - `Google Chrome Helper` (browser renderer process)
   - `launchd` (macOS init/system daemon, PID 1)

---

## Task 3.3 — Paths and Permissions

### Absolute vs Relative Paths

| Concept | Explanation | Example from Assignment |
| :--- | :--- | :--- |
| **Absolute path** | Full path from filesystem root (`/`) to the file/folder. Unambiguous, works from anywhere. | `/Users/[redacted]/digital-detective-1234/mission-03-operating-system` |
| **Relative path** | Path relative to current working directory. Shorter, depends on where you are. | `../mission-01-computer-basics` (from inside `mission-03`) |

**Commands used:** `pwd`, `cd ..`, `cd mission-01-computer-basics`

### File Permissions

**Permission breakdown for owner:**

| Permission | Letter | Meaning for File | Can Owner? |
| :--- | :--- | :--- | :--- |
| Read | `r` | View file contents (`cat`, open) | ✅ Yes |
| Write | `w` | Modify/delete file (`echo >`, `rm`) | ✅ Yes |
| Execute | `x` | Run as program/script (`./script.sh`) | ❌ No |

---

## Task 3.4 — Operating System Responsibilities

| OS Responsibility | Your Explanation | Example |
| :--- | :--- | :--- |
| **Process management** | The OS schedules CPU time, creates/terminates processes, and handles context switching so multiple programs appear to run simultaneously. | Running Chrome and VS Code at the same time; OS switches CPU between them. |
| **Memory management** | Allocates RAM to processes, handles virtual memory (swap), protects process memory from each other, and reclaims memory when programs exit. | When RAM is full, macOS swaps inactive apps to SSD to free space for active ones. |
| **Device management** | Provides drivers and abstraction layers so software can interact with hardware (disk, keyboard, GPU, network) without knowing hardware details. | Typing in a text editor: OS routes keystrokes from keyboard driver to the app. |
| **File management** | Organizes data into files/folders on storage, handles naming, permissions, and provides system calls (open, read, write, close). | Saving a document: OS writes bytes to SSD and updates filesystem metadata. |
| **User interface / shell** | Provides interfaces (GUI, CLI/shell) for users to launch programs, manage files, and interact with the system. | Terminal (zsh/bash) or Finder/Explorer — both talk to the OS kernel. |
| **Security and permissions** | Enforces access control (user/group/other), authentication, sandboxing, and isolation so processes/users can't access unauthorized resources. | `chmod 600 a.txt` — only owner can read/write; other users blocked. |

---

## Mission 3 Summary & Reflection

- **Commands learned:** `sw_vers`, `whoami`, `df -h`, `ps aux`, `top`, `pwd`, `cd`, `ls -l`.
- **Key concepts:** Process vs program, PID, absolute vs relative paths, permission triads (r/w/x), OS kernel responsibilities.
- **Challenges & Resolution:** ["No major issues."]
