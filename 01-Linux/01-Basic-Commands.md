# 🐧 Linux File Commands
 
**Covering:** `pwd` · `ls` · `cd` · `mkdir` · `touch` · `cp` · `mv` · `rm` · `cat`
 
---
 
## 1️⃣ `pwd` — Print Working Directory
 
To find our current directory in Linux, simply type the `pwd` command and press **Enter**. It prints the absolute path to our present location on the command line.
 
```bash
pwd
```
 
---
 
## 2️⃣ `ls` — List Directories
 
By default, the `ls` command lists the directories and files in our current directory. We can also specify a path to list the contents of a different directory. It's a versatile tool that can show detailed information about the files and directories we're viewing.
 
### 👻 Viewing Hidden Files
Not all files in a directory are visible by default. In Linux, filenames that start with a dot (`.`) are hidden. We can view them using the `-a` flag, which stands for **"all"**.
 
```bash
ls -a
```
 
### 📋 Getting Detailed Information
The `-l` flag stands for **"long"** and provides a detailed list of files. It shows, from left to right: file permissions, number of links, owner name, owner group, file size, timestamp of last modification, and the file/directory name.
 
```bash
ls -l
```
 
### 🔃 Sorting in Reverse Order
The `ls -r` command lists files and directories in **reverse alphabetical order** — handy for seeing the last items in a long list first.
 
```bash
ls -r
```
 
### 🔗 Combining Command Flags
Flags (also called arguments or options) can be combined into a single command, e.g., `ls -la`. The order of flags usually doesn't matter, so `ls -al` works identically. We can also add the reverse flag: `ls -lar`.
 
```bash
ls -la
ls -al
ls -lar
```
 
---
 
## 3️⃣ `cd` — Change Directories
 
The `cd` command is a built-in shell utility used to navigate through the filesystem hierarchy in Linux. To move to a sub-directory, we can use a relative path. Fortunately, the shell provides several shortcuts to make moving around much faster.
 
| Shortcut | Meaning |
|---|---|
| `cd .` | Current directory |
| `cd ..` | Parent directory — moves one level up |
| `cd ~` | Home directory (e.g., `/home/assignment2`) |
| `cd -` | Previous directory — goes back to the last one we were in |
 
---
 
## 4️⃣ `mkdir` — Make Directory
 
As we work with files, we need to organize them into directories. `mkdir` (short for **"Make Directory"**) lets us create a directory right from the terminal.
 
### 📁 Creating a Single Directory
The most basic use — creates a new directory in the current location if it doesn't already exist.
 
```bash
mkdir project
```
 
### 📁 Creating Multiple Directories
We can create several directories at once by listing their names, separated by spaces.
 
```bash
mkdir folder1 folder2 folder3
```
 
### 📁 Creating Nested Directories
The `-p` (**parent**) option creates a directory and its parent directories simultaneously, preventing errors if the parent directories don't exist.
 
```bash
mkdir -p books/hemingway/favorites
```
 
---
 
## 5️⃣ `touch` — Create Files & Update Timestamps
 
The `touch` command is a standard Unix-like utility. Its primary purpose is to change file timestamps, but it's also commonly used to create new, empty files.
 
### 📄 Creating New Files
The simplest way to create an empty file — if the file doesn't exist, `touch` creates it for us.
 
```bash
touch newfile.txt
```
 
### 🕐 Updating File Timestamps
The original function of `touch` is to update the access and modification timestamps of a file or directory. Using it on an existing file updates its timestamp to the current time.
 
### ⚙️ Advanced Timestamp Control
`touch` also provides options for more precise timestamp manipulation:
- `touch -t` — set a file's timestamp to a specific date and time
- `touch -d` — accepts various string formats for the date
---
 
## 6️⃣ `cp` — Copy
 
The `cp` command is the standard tool for copying files and directories. Basic syntax:
 
```bash
cp [source] [destination]
```
 
For example:
 
```bash
cp mysuperduperfile /home/purno/assignment2
```
 
Here, `mysuperduperfile` is the source file, and `/home/purno/assignment2` is the destination directory. We can also copy a file and give it a new name at the destination.
 
### 🌟 Using Wildcards for Bulk Copying
Wildcards are special characters that help select multiple files based on patterns:
 
| Wildcard | Meaning |
|---|---|
| `*` | Matches any sequence of characters |
| `?` | Matches any single character |
| `[ ]` | Matches any one of the characters enclosed in the brackets |
 
---
 
## 7️⃣ `mv` — Move
 
The `mv` command (short for **"move"**) serves two primary purposes: **renaming** files/directories and **moving** them to a different location. Its functionality is similar in many ways to `cp`.
 
### ✏️ Renaming Files and Directories
The syntax is straightforward — specify the old name and the new name.
 
```bash
mv oldname.txt newname.txt
```
 
### 📦 Moving Files and Directories
To move a single file into a different directory:
 
```bash
mv file.txt /home/purno/documents
```
 
By default, if we move a file to a destination where a file with the same name already exists, `mv` overwrites it **without warning**. To prevent accidental data loss, we can use these options:
 
| Option | Purpose |
|---|---|
| `-i` (interactive) | A crucial safety feature — prompts for confirmation before overwriting any existing file |
| `-b` (backup) | Creates a backup of the destination file (renamed with a `~` suffix) before overwriting |
| `-v` (verbose) | Prints out what it's doing, showing each file being moved or renamed |
 
---
 
## 8️⃣ `rm` — Remove
 
In Linux, it's common to accumulate files that are no longer needed. `rm` (**remove**) is the fundamental utility for deleting them.
 
### ⚠️ Understanding the Risk
`rm` is powerful, but that power comes with significant risk. Unlike graphical operating systems, Linux has **no recycle bin or trash can** for command-line deletions. Once we use `rm`, the files are **permanently gone**.
 
```bash
rm file.txt
```
 
### 🛡️ Using `rmdir` for Empty Directories
As a safer alternative, we can remove an **empty** directory with the `rmdir` command.
 
```bash
rmdir empty_folder
```
 
---
 
## 9️⃣ `cat` — Concatenate
 
The name `cat` is short for **"concatenate"**, hinting at its ability to link files together. Its most basic use is displaying the content of a single file directly in the terminal.
 
```bash
cat file.txt
```
 
We can also use `cat` with the output redirection operator (`>`) to create new files — a quick way to write text into a file directly from the terminal.
 
```bash
cat > newfile.txt
```
 
---
 
*✍️ Prepared as part of my Cybersecurity learning journey.*
