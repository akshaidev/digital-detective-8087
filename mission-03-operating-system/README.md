# Mission 3 - Understand the Operating System

## 1. Task / objective
Inspect operating system details, active processes, storage usage, file paths, and owner permissions, and summarize core OS responsibilities.

## 2. Work completed
* Ran system inspection commands (`uname`, `whoami`, `df -h`, `ps`, `top`, `ls -l`) and recorded privacy-redacted observations.
* Navigated between the repository root and `mission-03-operating-system` to compare absolute and relative paths.
* Inspected real owner permission bits on `terminal-practice/notes.txt` and completed the six-part OS responsibilities table.

## 3. Commands / tools used
* `uname -srm` — Displayed OS kernel name, release version, and CPU architecture.
* `whoami` & `id -u` — Checked the active user account identity (redacted in notes).
* `df -h /` — Displayed mounted root filesystem capacity, used space, and available storage.
* `ps -eo pid,comm` & `top` — Listed running processes, total process count, and Process IDs (PIDs).
* `ls -l terminal-practice/notes.txt` — Inspected actual file permission flags (`-rw-r--r--@`).

## 4. My understanding
### Task 3.1 — Exploring the Operating System
| Information explored | What it tells you | Your observation (privacy-safe) |
| :--- | :--- | :--- |
| Operating system / system details | Identifies the OS kernel, release version, and hardware architecture. | `Darwin 25.5.0 arm64` |
| Current account identity | Shows which user account owns the current shell session and its privileges. | Active user: [redacted] (UID 501) |
| Available and used storage | Reports total disk size, used space, free space, and mount points. | Root filesystem `/`: 460Gi total, 12Gi used, 42Gi available (22% capacity) |
| System activity snapshot | Shows currently executing programs and process counts. | Processes: 804 total, 5 running, 799 sleeping, 4165 threads  (804 processes listed via `ps`). |

### Task 3.2 — Understanding Processes
* **What is a process?** A process is an active instance of a program loaded into memory and being executed by the CPU, complete with its own memory space and system resources.
* **What does the PID column represent?** PID stands for **Process Identifier**—a unique integer assigned by the OS kernel to track, schedule, and manage each running process.
* **Examples of running processes observed:** Shell script runner `bash` (PID 3709), along with active processes from `ps`: `launchd` (PID 1), `logd` (PID 334).

### Task 3.3 — Paths and Permissions
* **Absolute vs. Relative Path:** An **absolute path** starts from the root directory (`/`) and uniquely locates a folder regardless of your current directory (for example, `/Users/[redacted]/Developer/NST/SnAI/Diwali_Project/digital-detective-8087` for the repository root and `/Users/[redacted]/Developer/NST/SnAI/Diwali_Project/digital-detective-8087/mission-03-operating-system` after running `cd mission-03-operating-system`). A **relative path** starts from your current working directory (such as `./mission-03-operating-system` from the root, or `..` to return from the subfolder).
* **Owner Permissions:** Inspecting `terminal-practice/notes.txt` with `ls -l` returned:
  `-rw-r--r--@ 1 [redacted]  staff  59 26 Nov 00:55 terminal-practice/notes.txt`
  The permission string is `-rw-r--r--@`. The owner's three permission characters are `rw-`, which means the owner **can read, can write, and cannot execute** the file.

| Permission | Meaning | Example |
| :--- | :--- | :--- |
| `r` - Read | Allows a file's contents to be read (or a directory's contents to be listed). | Opening a text file with `cat notes.txt`. |
| `w` - Write | Allows a file's contents to be modified (or files created/deleted in a directory). | Editing and saving `README.md`. |
| `x` - Execute | Allows a file to be run as a program; on a directory, allows entering (`cd`) into it. | Running a script like `./script.sh`. |

### Task 3.4 — Operating-System Responsibilities
| OS responsibility | Your explanation | Example |
| :--- | :--- | :--- |
| **Process management** | Schedules CPU time across running programs, creates/terminates processes, and handles multitasking. | Switching smoothly between Terminal and a web browser while code runs. |
| **Memory management** | Allocates and frees RAM for active processes while keeping process memory isolated. | Allocating RAM buffers to Python when running a script and reclaiming it on exit. |
| **Device management** | Communicates with hardware peripherals using device drivers and I/O queues. | Sending keystrokes from a USB/built-in keyboard to the active window. |
| **File management** | Organizes data into hierarchical directories, files, and metadata on storage drives. | Storing mission folders and tracking permissions on the SSD filesystem. |
| **User interface / shell** | Provides a way for users to interact with the OS via graphical windows or a command-line shell. | Typing commands into `zsh`/`bash` in Terminal or clicking icons in Finder. |
| **Security and permissions** | Enforces user authentication and file access rules so unauthorized users cannot alter system data. | Preventing standard user accounts from modifying system directories without privileges. |

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
* `mission-03-operating-system/README.md`
* `evidence/safe-outputs.txt`

## 8. Commit details
* **Commit message:** `Document operating system and file management`
* **Status:** Committed and pushed to GitHub on `main`.
