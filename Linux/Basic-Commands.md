# 🐧 Linux Basic Commands
 
Notes on essential Linux commands — organized by category for quick reference.
 
---
 
## 📁 File & Directory Management
 
| Command | Description | Example |
|---------|-------------|---------|
| `pwd` | Show current directory path | `pwd` |
| `ls` | List files and directories | `ls -la` |
| `cd` | Change directory | `cd /home/user` |
| `mkdir` | Create a new directory | `mkdir new_folder` |
| `rmdir` | Remove an empty directory | `rmdir old_folder` |
| `rm` | Remove files/directories | `rm -rf folder/` |
| `cp` | Copy files/directories | `cp file1.txt file2.txt` |
| `mv` | Move or rename files | `mv old.txt new.txt` |
| `touch` | Create an empty file | `touch notes.txt` |
| `find` | Search for files | `find / -name "*.txt"` |
| `locate` | Quickly find files by name | `locate passwd` |
 
---
 
## 📄 Viewing & Editing Files
 
| Command | Description | Example |
|---------|-------------|---------|
| `cat` | Display file content | `cat file.txt` |
| `less` | View file page by page | `less file.txt` |
| `head` | Show first lines of a file | `head -n 10 file.txt` |
| `tail` | Show last lines of a file | `tail -f log.txt` |
| `nano` | Simple terminal text editor | `nano file.txt` |
| `vim` | Advanced terminal text editor | `vim file.txt` |
| `grep` | Search text inside files | `grep "error" log.txt` |
 
---
 
## 🔐 Permissions & Ownership
 
| Command | Description | Example |
|---------|-------------|---------|
| `chmod` | Change file permissions | `chmod 755 script.sh` |
| `chown` | Change file owner | `chown user:group file.txt` |
| `sudo` | Run command as superuser | `sudo apt update` |
| `whoami` | Show current logged-in user | `whoami` |
 
---
 
## 👤 Users & Groups
 
| Command | Description | Example |
|---------|-------------|---------|
| `adduser` | Add a new user | `adduser john` |
| `passwd` | Change user password | `passwd john` |
| `usermod` | Modify a user account | `usermod -aG sudo john` |
| `groups` | Show groups of a user | `groups john` |
| `su` | Switch user | `su john` |
 
---
 
## ⚙️ Process Management
 
| Command | Description | Example |
|---------|-------------|---------|
| `ps` | Show running processes | `ps aux` |
| `top` | Real-time process monitor | `top` |
| `kill` | Terminate a process by PID | `kill 1234` |
| `killall` | Terminate process by name | `killall firefox` |
| `jobs` | List background jobs | `jobs` |
| `bg` / `fg` | Resume job in background/foreground | `bg %1` |
 
---
 
## 💾 Disk & System Info
 
| Command | Description | Example |
|---------|-------------|---------|
| `df` | Show disk space usage | `df -h` |
| `du` | Show directory size | `du -sh folder/` |
| `free` | Show memory usage | `free -h` |
| `uname` | Show system information | `uname -a` |
| `uptime` | Show system uptime | `uptime` |
 
---
 
## 🌐 Networking Basics
 
| Command | Description | Example |
|---------|-------------|---------|
| `ping` | Check network connectivity | `ping google.com` |
| `ifconfig` / `ip a` | Show network interfaces | `ip a` |
| `netstat` | Show network connections | `netstat -tulnp` |
| `curl` | Transfer data from/to a server | `curl -I https://example.com` |
| `wget` | Download files from the web | `wget https://example.com/file.zip` |
| `ssh` | Connect to remote machine | `ssh user@192.168.1.10` |
| `scp` | Copy files over SSH | `scp file.txt user@host:/path/` |
 
---
 
## 📦 Package Management (Debian/Ubuntu)
 
| Command | Description | Example |
|---------|-------------|---------|
| `apt update` | Update package list | `sudo apt update` |
| `apt upgrade` | Upgrade installed packages | `sudo apt upgrade` |
| `apt install` | Install a package | `sudo apt install nmap` |
| `apt remove` | Remove a package | `sudo apt remove nmap` |
 
---
 
## 🗜️ Compression & Archiving
 
| Command | Description | Example |
|---------|-------------|---------|
| `tar` | Archive files | `tar -cvf archive.tar folder/` |
| `tar -x` | Extract archive | `tar -xvf archive.tar` |
| `zip` | Compress files into .zip | `zip archive.zip file.txt` |
| `unzip` | Extract .zip file | `unzip archive.zip` |
 
---
 
## 💡 Useful Shortcuts
 
| Shortcut | Action |
|----------|--------|
| `Ctrl + C` | Stop current command |
| `Ctrl + Z` | Suspend current command |
| `Ctrl + R` | Search command history |
| `Tab` | Auto-complete command/filename |
| `!!` | Repeat last command |
 
---
 
## 📝 Notes
 
> Add your own personal notes, examples, or gotchas here as you practice these commands.
 
---
 
*Part of my [Cybersecurity-Notes](../README.md) repository.*
 
