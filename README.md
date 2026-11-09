# Digital Detective — Diwali Independent Learning Assignment

## Overview
This repository contains my complete submission for the **Digital Detective** assignment. The goal was to investigate computer fundamentals, practice terminal operations, understand operating system internals, explore data representation, and demonstrate Git/GitHub workflows — all documented as a sequence of 8 missions.

**Student:** [Ujjwal Dubey]
**USN:** [8415]
**Repository:** `digital-detective-8415`

---

## Mission Index

| Mission | Title | Folder | Key Deliverables |
| :--- | :--- | :--- | :--- |
| 0 | Repository & Workspace Setup | [`mission-00-setup`](mission-00-setup/README.md) | Repo structure, tool versions |
| 1 | Computer Fundamentals & IPOS | [`mission-01-computer-basics`](mission-01-computer-basics/README.md) | IPOS trace, hardware/software tables, everyday systems |
| 2 | Terminal & File Management | [`mission-02-terminal`](mission-02-terminal/README.md) | Command reference, flags/pipes, package managers |
| 3 | OS, Processes & Permissions | [`mission-03-operating-system`](mission-03-operating-system/README.md) | System info, processes, paths, permissions, OS responsibilities |
| 4 | How Programs Run | [`mission-04-programs`](mission-04-programs/README.md) | `hello.py`, compiler vs interpreter comparison |
| 5 | Numbers & Data | [`mission-05-numbers-data`](mission-05-numbers-data/README.md) | Manual conversions, Python verification, `number_converter.py`, text encoding |
| 6 | Git & GitHub | [`mission-06-git-github`](mission-06-git-github/README.md) | Git workflow, branch `update-about`, Pull Request, glossary |
| 7 | Computer Networks | [`mission-07-networking`](mission-07-networking/README.md) | Network concepts, `ping`/`dig`, website request flow |
| 8 | Final Report | [`mission-08-final-report`](mission-08-final-report/README.md) | Repository verification, submission checklist |

---

## Topics Explored
- **Computer Architecture:** IPOS cycle, hardware vs software classification, embedded systems
- **Command Line:** Navigation, file ops, redirection, pipes, flags, Homebrew
- **Operating Systems:** Processes, memory, storage, paths, permissions, kernel responsibilities
- **Program Execution:** Interpreters vs compilers, Python runtime
- **Data Representation:** Binary/hex/decimal conversion, ASCII/UTF-8 encoding
- **Version Control:** Git workflow, branching, pull requests, collaboration
- **Networking:** LAN/MAN/WAN, DNS, routing, HTTP/TCP/TLS, packet switching

---

## Running the Number Converter

```bash
cd mission-05-numbers-data
python3 number_converter.py
# Enter a positive integer when prompted (e.g., 13, 255, 1024)

Sample run:
Enter a positive decimal integer: 255
Decimal:   255
Binary:    11111111
Hexadecimal: FF

---

Learning Summary

Through this assignment I learned:
1. How data flows through a computer via Input → Processing → Output → Storage.
2. Practical terminal skills — navigating, managing files, using pipes/flags, and installing tools via Homebrew.
3. OS internals — processes, virtual memory, file permissions, and kernel roles.
4. The difference between compiled and interpreted languages, and how Python executes code.
5. Number systems — manual base conversion, Python's bin()/hex()/int(), and why encoding standards (ASCII/UTF-8) exist.
6. Git collaboration — staging, committing, branching, and using Pull Requests for code review.
7. Network fundamentals — DNS resolution, connectivity testing, and the 7-step HTTPS request flow.

▎ Note: Each mission was completed, documented in its folder, committed with a meaningful message, and pushed to GitHub separately — following the required sequential workflow.

---

Repository Quality

- ✅ All 8 mission folders present with READMEs
- ✅ Required code files (hello.py, number_converter.py) included
- ✅ Meaningful commit history (one per mission minimum)
- ✅ Branch update-about and Pull Request visible on GitHub
- ✅ No personal information (usernames, IPs, device names) in any file
- ✅ All commits pushed to public GitHub repository

---
