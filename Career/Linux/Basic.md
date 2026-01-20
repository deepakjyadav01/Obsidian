
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

