
# Basic commands

### `pwd`

**Explanation:** Prints the full path of the current working directory.  
**Example:**

```bash
pwd
# Output: /home/bob/projects
```

---

### `ls`

**Explanation:** Lists files and directories in the current directory.  
**Example:**

```bash
ls
# Output: file1.txt  app.py  logs/
```

---

### `cd`

**Explanation:** Changes the current working directory.  
**Example:**

```bash
cd /var/log
```

---

### `clear`

**Explanation:** Clears the terminal screen for a clean view.  
**Example:**

```bash
clear
```

---

### `history`

**Explanation:** Displays previously executed commands in the current shell.  
**Example:**

```bash
history
# Output:  101 ls
#          102 cd /var
```

---

### `exit`

**Explanation:** Exits the current shell or SSH session.  
**Example:**

```bash
exit
```



---

### `touch`

**Explanation:** Creates an empty file or updates the timestamp of an existing file.  
**Example:**

```bash
touch notes.txt
```

---

### `mkdir`

**Explanation:** Creates a new directory.  
**Example:**

```bash
mkdir projects
```

---

### `rmdir`

**Explanation:** Deletes an **empty** directory.  
**Example:**

```bash
rmdir old_folder
```

---

### `cp`

**Explanation:** Copies files or directories from one location to another.  
**Example:**

```bash
cp file.txt backup.txt
```

---

### `mv`

**Explanation:** Moves or renames files and directories.  
**Example:**

```bash
mv old.txt new.txt
```

---

### `rm`

**Explanation:** Deletes files or directories permanently.  
**Example:**

```bash
rm file.txt
```

---

### `tree`

**Explanation:** Displays directories and files in a tree-like structure.  
**Example:**

```bash
tree .
```

---

### `stat`

**Explanation:** Shows detailed information about a file or directory.  
**Example:**

```bash
stat file.txt
```

---

### `file`

**Explanation:** Determines the type of a file.  
**Example:**

```bash
file script.sh
# Output: Bourne-Again shell script
```


### `cat`

**Explanation:** Displays the contents of a file (or concatenates multiple files).  
**Example:**

```bash
cat file.txt
```

---

### `less`

**Explanation:** Views file content one screen at a time with scrolling.  
**Example:**

```bash
less /var/log/syslog
```

---

### `more`

**Explanation:** Displays file content page by page (older, less flexible than `less`).  
**Example:**

```bash
more file.txt
```

---

### `head`

**Explanation:** Shows the first 10 lines of a file by default.  
**Example:**

```bash
head file.txt
```

---

### `tail`

**Explanation:** Shows the last 10 lines of a file by default.  
**Example:**

```bash
tail file.txt
```

---

### `watch`

**Explanation:** Runs a command repeatedly and shows live updates.  
**Example:**

```bash
watch df -h
```

---

### `wc`

**Explanation:** Counts lines, words, and characters in a file.  
**Example:**

```bash
wc file.txt
```

---


# Permission

### `chmod`

**Explanation:** Changes file or directory permissions (read, write, execute).  
**Example:**

```bash
chmod 755 script.sh
```

---

### `chown`

**Explanation:** Changes the owner of a file or directory.  
**Example:**

```bash
chown bob file.txt
```

---

### `chgrp`

**Explanation:** Changes the group ownership of a file or directory.  
**Example:**

```bash
chgrp developers file.txt
```

---

### `umask`

**Explanation:** Sets the default permission mode for newly created files and directories.  
**Example:**

```bash
umask 022
```

---

### Super important interview insight (simple)

- `chmod` → **who can access**
    
- `chown` → **who owns**
    
- `chgrp` → **which group**
    
- `umask` → **default permissions going forward**
    

Here are **one-line explanations** with **one simple example** for each command 👇

---

# Filtering

### `grep`

**Explanation:** Searches for a text pattern inside files.  
**Example:**

```bash
grep "error" app.log
```

---

### `egrep`

**Explanation:** Searches using **extended regular expressions** (same as `grep -E`).  
**Example:**

```bash
egrep "error|failed" app.log
```

---

### `fgrep`

**Explanation:** Searches for **fixed strings only** (no regex, same as `grep -F`).  
**Example:**

```bash
fgrep "ERROR[123]" app.log
```

---

### `find`

**Explanation:** Searches for files and directories based on conditions (name, size, time, etc.).  
**Example:**

```bash
find /var/log -name "*.log"
```

---

### `locate`

**Explanation:** Finds files quickly using a prebuilt database.  
**Example:**

```bash
locate ssh_config
```

---

### `which`

**Explanation:** Shows the full path of a command being executed.  
**Example:**

```bash
which python
```

---

### `whereis`

**Explanation:** Locates the binary, source, and manual pages of a command.  
**Example:**

```bash
whereis ls
```

---

### ⚡ Interview gold (remember this)

- `grep` → **search inside files**
    
- `find` → **search files themselves**
    
- `locate` → **fast but database-based**
    
- `which` → **which command runs**
    
- `whereis` → **everything related to a command**
    


### `awk`

**Explanation:** Pattern-scanning and text-processing language for structured data.  
**Example:**

```bash
awk '{print $1}' data.txt
```

---

### `sed`

**Explanation:** Stream editor used to search, replace, and modify text.  
**Example:**

```bash
sed 's/error/ERROR/g' app.log
```

---

### `cut`

**Explanation:** Extracts specific columns or fields from text.  
**Example:**

```bash
cut -d',' -f1 users.csv
```

---

### `sort`

**Explanation:** Sorts lines of text alphabetically or numerically.  
**Example:**

```bash
sort names.txt
```

---

### `uniq`

**Explanation:** Filters out repeated lines (works on sorted input).  
**Example:**

```bash
sort data.txt | uniq
```

---

### `tr`

**Explanation:** Translates or deletes characters from input.  
**Example:**

```bash
tr 'a-z' 'A-Z' < file.txt
```

---

### `xargs`

**Explanation:** Builds and executes commands from standard input.  
**Example:**

```bash
cat files.txt | xargs rm
```

---

### `paste`

**Explanation:** Merges lines from multiple files side by side.  
**Example:**

```bash
paste file1.txt file2.txt
```

---

### `column`

**Explanation:** Formats output into aligned columns for readability.  
**Example:**

```bash
column -t data.txt
```

---

## 🧠 Mental model (IMPORTANT)

|Command|Purpose|
|---|---|
|`grep`|filter rows|
|`awk`|pick columns|
|`sed`|clean text|
|`sort`|prepare for counting|
|`uniq -c`|count|

# Networking

---

### `ssh`

**Explanation:** Securely connects to a remote machine over the network.  
**Example:**

`ssh bob@192.168.1.10`

---

### `scp`

**Explanation:** Securely copies files between local and remote systems.  
**Example:**

`scp file.txt bob@192.168.1.10:/home/bob/`

---

### `rsync`

**Explanation:** Efficiently syncs files and directories locally or remotely.  
**Example:**

`rsync -avz project/ bob@192.168.1.10:/home/bob/project/`

---

### `curl`

**Explanation:** Transfers data from or to a server (commonly used for APIs).  
**Example:**

`curl https://example.com`

---

### `wget`

**Explanation:** Downloads files from the web.  
**Example:**

`wget https://example.com/file.zip`

---

### `ping`

**Explanation:** Checks network connectivity to a host.  
**Example:**

`ping google.com`

---

### `netstat`

**Explanation:** Displays network connections, routing tables, and ports (legacy).  
**Example:**

`netstat -tuln`

---

### `ss`

**Explanation:** Shows active socket connections (modern replacement for netstat).  
**Example:**

`ss -tuln`

---

### `nc` (netcat)

**Explanation:** Reads/writes data over TCP/UDP (network debugging tool).  
**Example:**

`nc -zv localhost 80`

---

## 🧠 Interview cheat sheet

| Command | When to use         |
| ------- | ------------------- |
| `ssh`   | connect to server   |
| `scp`   | copy files securely |
| `rsync` | sync folders        |
| `curl`  | API testing         |
| `wget`  | file download       |
| `ping`  | connectivity check  |
| `ss`    | check open ports    |
| `nc`    | test ports/services |

# Environment & variables

### `apt`

**Explanation:** Modern package manager for Debian/Ubuntu systems (user-friendly).  
**Example:**

`sudo apt install nginx`

---

### `apt-get`

**Explanation:** Low-level, script-friendly package manager for Debian/Ubuntu.  
**Example:**

`sudo apt-get update`

---

### `yum`

**Explanation:** Legacy package manager for RHEL/CentOS 7 and earlier.  
**Example:**

`sudo yum install httpd`

---

### `dnf`

**Explanation:** Modern replacement for `yum` on RHEL/CentOS 8+, Fedora.  
**Example:**

`sudo dnf install docker`

---

### `brew` (macOS)

**Explanation:** Package manager for macOS to install CLI tools and apps.  
**Example:**

`brew install node`

---

### `env`

**Explanation:** Runs a command with a modified environment or prints environment variables.  
**Example:**

`env`

---

### `printenv`

**Explanation:** Prints environment variables and their values.  
**Example:**

`printenv PATH`

---

### `export`

**Explanation:** Makes a variable available to child processes.  
**Example:**

`export APP_ENV=production`

---

### `set`

**Explanation:** Displays shell variables and functions (also used to set options).  
**Example:**

`set | grep PATH`

---

### `unset`

**Explanation:** Removes a variable or function.  
**Example:**

`unset APP_ENV`

---

### `alias`

**Explanation:** Creates a shortcut for a command.  
**Example:**

`alias ll='ls -la'`

---

### `unalias`

**Explanation:** Removes an existing alias.  
**Example:**

`unalias ll`

---

# Script execution
### `bash`

**Explanation:** Starts a new Bash shell or runs a script using Bash.  
**Example:**

`bash script.sh`

---

### `sh`

**Explanation:** Runs a script using the system’s default POSIX shell.  
**Example:**

`sh script.sh`

---

### `source`

**Explanation:** Executes a script in the **current shell** (no new process).  
**Example:**

`source ~/.bashrc`

---

### `exec`

**Explanation:** Replaces the current shell process with another command.  
**Example:**

`exec bash`

---

### `set -x`

**Explanation:** Prints each command before executing it (debug mode).  
**Example:**

`set -x`

---

### `set -e`

**Explanation:** Exits the script immediately if any command fails.  
**Example:**

`set -e`

---

### `trap`

**Explanation:** Runs a command when the script receives a signal or exits.  
**Example:**

`trap "echo Script exiting" EXIT`

---

##  Interview-level understanding (VERY IMPORTANT)

|Feature|Why it matters|
|---|---|
|`source`|Load env vars into current shell|
|`exec`|Used in Docker ENTRYPOINT|
|`set -e`|Fail fast in CI/CD|
|`set -x`|Debug production scripts|
|`trap`|Cleanup temp files|

---