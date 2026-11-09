# Mission 2: Terminal and File Management

## Task 2.1 — Basic Terminal Operations

| Operation / Command Name | Command Used | What it does | What I Observed |
| :--- | :--- | :--- | :--- |
| Current-directory display | `pwd` | Prints the absolute path of the current working directory | [/Users/ujjwaldubey/digital-detective-8415`] |
| Directory listing | `ls` | Lists files and folders in the current location | [`README.md mission-00-setup mission-01-computer-basics ...`] |
| Detailed listing | `ls -la` | Lists all entries (including hidden) with permissions, owner, size, date | [shows `.git`, `.DS_Store`, permission strings like `-rw-r--r--`] |
| Change directory | `cd ..` | Moves to the parent directory | [Your observation — e.g., prompt changes from `digital-detective-1234` to parent folder name] |
| Create directory | `mkdir terminal-practice` | Creates a new empty folder | [folder appears in `ls` output] |
| Create empty file | `touch terminal-practice/notes.txt` | Creates an empty file (or updates timestamp) | [file appears inside `terminal-practice/`] |
| Copy file | `cp terminal-practice/notes.txt terminal-practice/notes-backup.txt` | Duplicates a file with a new name | [both files now exist with same size] |
| Move / rename file | `mv terminal-practice/notes-backup.txt terminal-practice/notes-renamed.txt` | Renames or moves a file | [old name gone, new name appears] |
| Display file contents | `cat terminal-practice/notes.txt` | Outputs the entire file content to terminal | [empty output, or text if you added content] |

---

## Task 2.2 — Practise File Changes Safely

**Commands executed:**
```bash
echo "First line of text" > terminal-practice/notes.txt
echo "Second line added" >> terminal-practice/notes.txt
cat terminal-practice/notes.txt
cp terminal-practice/notes.txt terminal-practice/notes-backup.txt
mv terminal-practice/notes-backup.txt terminal-practice/notes-backup-renamed.txt

Output observed:
[First line of text
Second line added]

Answers:
1. Replacing vs. Adding: Using > (redirection) overwrites the entire file content, destroying previous data. Using >> appends new content to the end of the file, preserving existing lines.
2. Copy vs. Move: cp creates a duplicate — both the original and the copy exist independently. mv relocates or renames — the original name/path ceases to exist; only the new one remains.
3. Current-directory display (pwd): Provides the absolute path from the filesystem root to the current working directory, confirming exactly where subsequent commands will read/write.
4. Directory listing (ls): Reveals the names (and with flags, metadata) of files and subdirectories in the current location, enabling navigation, verification of operations, and discovery of hidden items.

---

Task 2.3 — Flags and Pipes

Flags Exploration

ls          # Basic listing
ls -lah     # Detailed (-l), hidden (-a), human-readable sizes (-h)

What changed:
- -l (long format): Adds file permissions, link count, owner, group, size in bytes, modification timestamp.
- -a (all): Reveals hidden entries starting with . (e.g., .git, .DS_Store).
- -h (human-readable): Converts byte counts to K, M, G suffixes (e.g., 4.0K instead of 4096).

Pipe Exploration

ls -la | head -5

Explanation:
The pipe symbol (|) connects the standard output (stdout) of the command on the left (ls -la) to the standard input (stdin) of the command on the right (head -5).
- Left side produces a full detailed directory listing.
- Right side consumes that listing and emits only the first 5 lines.
  This allows chaining commands to filter, transform, or limit data without creating temporary files.

---

Task 2.4 — Package Managers

Homebrew check: 
brew --version

Output observed:
[Homebrew 7.0.12]

Why package managers are useful:
Package managers automate the installation, updating, and removal of software while automatically resolving dependencies (required libraries or other packages). They provide a centralized, searchable repository of vetted packages, reducing the risk of downloading incompatible or malicious software. On macOS, Homebrew simplifies installing command-line tools and development libraries that are not included by default in the operating system.
