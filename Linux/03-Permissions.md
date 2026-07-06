# 🔐 Linux Users, Groups & Permissions
 
**Covering:** `r`, `w`, `x` · `chmod` · `chown` · `chgrp`
 
---
 
## 📜 Understanding Permission Strings
 
When we list files in a detailed format (`ls -l`), we see a string of characters that define their permissions.
 
- **`r`** → Read permission
- **`w`** → Write permission
- **`x`** → Execute permission
The permission string has **four main parts**. The first character indicates the file type:
 
- **`d`** → Directory
- **`-`** (hyphen) → Regular file
The remaining nine characters are split into three groups of three (`rwx`), representing permissions for the **user (owner)**, the **group**, and **others**, in that order.
 
```
d rwx r-x r--
│ │   │   └── Others
│ │   └────── Group
│ └────────── User (Owner)
└──────────── File type (d = directory)
```
 
---
 
## 1️⃣ `chmod` — Change Mode
 
We can control a directory's or file's permissions using the `chmod` command.
 
### 🔢 Numerical (Octal) Mode
The most powerful way to change permissions in Linux is through **numerical/octal mode**. This method allows setting all permissions for the **user**, **group**, and **others** simultaneously with a three-digit number.
 
| Value | Permission |
|---|---|
| `4` | Read (`r`) |
| `2` | Write (`w`) |
| `1` | Execute (`x`) |
 
To set a permission, we **add the numbers together**. For example, granting read, write, and execute means `4 + 2 + 1 = 7`.
 
### ✅ Example 1 — Full Permissions (777)
Giving all (`r`, `w`, `x`) permissions to a directory named `C++`:
 
```bash
chmod 777 C++
```
 
| Target | Calculation | Result |
|---|---|---|
| User | 4 + 2 + 1 | `rwx` |
| Group | 4 + 2 + 1 | `rwx` |
| Others | 4 + 2 + 1 | `rwx` |
 
### ⚙️ Example 2 — Restricted Permissions (755)
Not giving all (`r`, `w`, `x`) permissions to a directory named `ostad`:
 
```bash
chmod 755 ostad
```
 
| Target | Calculation | Result |
|---|---|---|
| User | 4 + 2 + 1 | `rwx` |
| Group | 4 + 0 + 1 | `r-x` |
| Others | 4 + 0 + 1 | `r-x` |
 
---
 
## 2️⃣ `chown` — Change Owner
 
While `chmod` controls **what** permissions exist, `chown` (short for **"change owner"**) controls **who** owns the file or directory in the first place. It lets us transfer ownership of a file/directory from one user to another.
 
### 👤 Changing the Owner Only
 
```bash
chown purno file.txt
```
 
This makes `purno` the new owner of `file.txt`.
 
### 👥 Changing the Owner and Group Together
 
```bash
chown purno:developers project/
```
 
This sets `purno` as the owner **and** `developers` as the group of the `project` directory, all in one command.
 
### 🔁 Applying Recursively
To change ownership of a directory **and everything inside it** (all sub-folders and files), we use the `-R` (recursive) flag:
 
```bash
chown -R purno:developers project/
```
 
> ⚠️ **Note:** In most systems, only the **root user** (or a user with `sudo`) can change ownership to another user, since this affects system security and access control.
 
---
 
## 3️⃣ `chgrp` — Change Group
 
`chgrp` (short for **"change group"**) is a more focused command — it changes **only the group** associated with a file or directory, without touching the owner.
 
### 👥 Changing the Group
 
```bash
chgrp developers project/
```
 
This sets the group of `project` to `developers`, while the owner stays the same.
 
### 🔁 Applying Recursively
 
```bash
chgrp -R developers project/
```
 
This changes the group for the `project` directory and everything inside it.
 
### 🆚 `chown` vs `chgrp`
 
| Command | Changes Owner? | Changes Group? |
|---|---|---|
| `chown user file` | ✅ Yes | ❌ No |
| `chown user:group file` | ✅ Yes | ✅ Yes |
| `chgrp group file` | ❌ No | ✅ Yes |
 
---
 
## 📝 Summary
 
| Command | Purpose |
|---|---|
| `chmod` | Changes **what** a user/group/others can do (read, write, execute) |
| `chown` | Changes **who** owns a file or directory |
| `chgrp` | Changes **which group** a file or directory belongs to |
 
Together, these three commands give complete control over Linux file security — deciding **who owns** something, **which group** it belongs to, and **what actions** are allowed on it.
 
---
 
*✍️ Prepared as part of my Cybersecurity learning journey.*
