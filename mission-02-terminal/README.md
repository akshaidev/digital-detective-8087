# Mission 2 - Become Comfortable with the Terminal

## 1. Task / objective
Practice core command-line navigation and file management inside a safe sandbox folder, understand command flags and pipes, and inspect a package manager.

## 2. Work completed
* Executed directory navigation, file creation, copying, moving, and inspection commands directly in Terminal.
* Created `terminal-practice/` using `mkdir`, initialized `notes.txt` with `touch`, tested overwriting (`>`) vs. appending (`>>`), and created `notes-backup.txt`.
* Compared standard `ls` output against `ls -lah` and piped `ls -l` into `head -n 5`.
* Checked package manager availability safely without installing or removing software.

## 3. Commands / tools used
* `pwd`, `ls`, `ls -l`, `ls -lah`, `cd ..`, `mkdir`, `touch`, `cp`, `mv`, `cat`, `head` — Core POSIX file and directory utilities.
* `|` (Pipe operator) — Redirects standard output of one command into standard input of the next.
* `brew --version` & `brew list` — Checked Homebrew installation status and viewed the list of managed packages (when installed).

## 4. My understanding
### Task 2.1 — Basic Terminal Operations
| Operation / command name | What it does | What I observed |
| :--- | :--- | :--- |
| Current-directory display (`pwd`) | Prints the full absolute path of the current working directory. | Displayed `/Users/[redacted]/Developer/NST/SnAI/Diwali_Project/digital-detective-8087` |
| Directory listing (`ls`) | Lists visible files and folders in the current directory. | Listed 11 items including `evidence mission-00-setup mission-01-computer-basics mission-02-terminal`. |
| Detailed listing (`ls -l`) | Displays permissions, owner, file size in bytes, and modification date. | Returned 12 lines including the `total` header and item metadata. |
| Change directory (`cd ..`) | Moves the shell session up one level to the parent directory. | `pwd` changed to `/Users/[redacted]/Developer/NST/SnAI/Diwali_Project` before returning to `digital-detective-8087`. |
| Create directory (`mkdir`) | Creates a new empty folder at the specified path. | Created `terminal-practice` without errors. |
| Create empty file (`touch`) | Creates a zero-byte file or updates its timestamp if it exists. | Created `terminal-practice/notes.txt` with initial size 0 bytes. |
| Copy file (`cp`) | Duplicates a file to a new path while keeping the original intact. | Copied `notes.txt` to `notes-copy.txt` with both present. |
| Move / rename file (`mv`) | Moves a file to a new directory or renames it in place. | Renamed `notes-copy.txt` to `notes-backup.txt`. |
| Display file contents (`cat`) | Reads a file and prints its text contents directly to the terminal. | Printed 2 lines: `First line of practice notes. Second line appended safely.` |

### Task 2.2 — Safe File Practice Questions
* **Replacing vs. adding text:** Using `>` truncates (overwrites) the file before writing new text, whereas `>>` appends new text to the end of the file while preserving existing lines.
* **Copying vs. moving a file:** `cp` creates an independent duplicate leaving the source file untouched; `mv` relocates or renames the original file so only one copy remains.
* **Current-directory display (`pwd`):** Shows your exact location in the directory tree from the root (`/`), preventing accidental edits in the wrong folder.
* **Why directory listing (`ls`) is useful:** Lets you immediately verify file names, folder structure, hidden files, and permissions directly from the keyboard.

### Task 2.3 — Flags and Pipes
* **Flags (`ls` vs. `ls -lah`):** Plain `ls` showed 11 visible entries. Running `ls -lah` produced 16 lines because `-a` revealed hidden entries (`.`, `..`, `.git`), `-l` added metadata columns, and `-h` formatted sizes into human-readable units.
* **Pipes (`ls -l | head -n 5`):** The pipe symbol (`|`) sends the standard output (`stdout`) of `ls -l` into the standard input (`stdin`) of `head -n 5`, filtering the output to only the first 5 lines:

```text
total 8
drwxr-xr-x@ 3 [redacted]  staff    96 26 Nov 00:55 evidence
drwxr-xr-x@ 3 [redacted]  staff    96 26 Nov 00:55 mission-00-setup
drwxr-xr-x@ 3 [redacted]  staff    96 26 Nov 00:55 mission-01-computer-basics
drwxr-xr-x@ 3 [redacted]  staff    96 26 Nov 00:55 mission-02-terminal
```

### Task 2.4 — Package Managers
Package managers (such as Homebrew on macOS or `apt` on Ubuntu) automate downloading, verifying, installing, updating, and removing command-line tools and libraries from trusted repositories. Homebrew is installed (`Homebrew 7.0.14`). Managed packages viewed via `brew list`: `abseil, ada-url, aom, brotli, c-ares, ca-certificates, cairo, chafa, cowsay, dav1d, eza, ffmpeg, fmt, fontconfig, freetype, fribidi, fzf, gdk-pixbuf, gemini-cli, gettext, gh, giflib, glib, graphite2, harfbuzz, hdrhistogram_c, highway, icu4c@78, icu4c@79, imath, jpeg-turbo, jpeg-xl, json-c, lame, libavif, libdatrie, libdeflate, libffi, libgit2, libnghttp2, libnghttp3, libngtcp2, libpng, librsvg, libssh2, libthai, libtiff, libunistring, libusb, libuv, libvmaf, libvpx, libx11, libxau, libxcb, libxdmcp, libxext, libxrender, little-cms2, llhttp, lz4, lzo, merve, mpg123, mysql, nbytes, node, openexr, openjdk, openjdk@21, openjph, openssl@3, openssl@4, opus, pango, pcre2, pixman, protobuf, rclone, readline, scrcpy, sdl2-compat, sdl3, simdjson, simdutf, sqlite, svt-av1, tokei, tree, uvwasi, webp, x264, x265, xorgproto, xz, zlib-ng-compat, zstd, android-platform-tools, android-studio, desktoppr, docker-desktop, font-jetbrains-mono-nerd-font, font-meslo-lg-nerd-font, ollama-app, zerotier-one`.

## 5. Difficulties faced
No major difficulties.

## 6. How I resolved them
Not applicable.

## 7. Evidence / files
* `mission-02-terminal/README.md`
* `terminal-practice/notes.txt`
* `terminal-practice/notes-backup.txt`
* `evidence/safe-outputs.txt`

## 8. Commit details
* **Commit message:** `Complete Terminal and file management mission`
* **Status:** Committed and pushed to GitHub on `main`.
