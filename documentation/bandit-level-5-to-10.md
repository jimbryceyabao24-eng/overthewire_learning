# OverTheWire Bandit: Levels 5–10

## Overview

This documentation covers Bandit Levels 5 to 10 from OverTheWire. These challenges focus on important Linux commands for searching files, checking file properties, filtering text, identifying unique lines, and extracting readable information.

## Level 5 → Level 6: Finding Files by Properties

**Objective:** Find a human-readable, non-executable file that is exactly 1,033 bytes inside the `inhere` directory.

**Command:**
```bash
cd inhere
find . -type f -size 1033c ! -executable
```

**Important details:**
- `cd inhere` enters the target directory.
- `find` searches for files and directories.
- `-type f` searches regular files.
- `-size 1033c` finds files exactly 1,033 bytes.
- `! -executable` excludes executable files.

Use `cat` with the discovered file path to read its contents.

## Level 6 → Level 7: Searching the Entire Filesystem

**Objective:** Find a file owned by user `bandit7`, group `bandit6`, and exactly 33 bytes in size.

**Command:**
```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

**Important details:**
- `/` searches from the root directory.
- `-type f` searches regular files.
- `-user bandit7` specifies the file owner.
- `-group bandit6` specifies the group owner.
- `-size 33c` finds files exactly 33 bytes.
- `2>/dev/null` hides error messages, such as permission-denied errors.

Use `cat` with the discovered file path to read its contents.

## Level 7 → Level 8: Searching for Specific Text

**Objective:** Find the password in `data.txt`, located next to the word `millionth`.

**Command:**
```bash
grep "millionth" data.txt
```

**Important details:**
- `grep` searches for specific text inside files.
- `"millionth"` is the keyword being searched.
- `data.txt` is the file being examined.
- The matching line displays the keyword and its corresponding password.

## Level 8 → Level 9: Finding a Unique Line

**Objective:** Find the only line that appears exactly once in `data.txt`.

**Command:**
```bash
sort data.txt | uniq -u
```

**Important details:**
- `sort` arranges lines alphabetically.
- `|` (pipe) sends the output of one command to another.
- `uniq -u` displays lines that occur only once.
- Sorting first is necessary because `uniq` checks adjacent lines.

## Level 9 → Level 10: Extracting Readable Strings

**Objective:** Find the password among human-readable strings in `data.txt`. The password is preceded by several equal signs (`=`).

**Command:**
```bash
strings data.txt | grep "==="
```

**Important details:**
- `strings` extracts readable text from binary files.
- `grep` filters the output for lines containing equal signs.
- `data.txt` is the file being examined.
- Combining commands with a pipe makes searching more efficient.

## Important Linux Commands Learned

| Command | Purpose |
|---|---|
| `cd` | Change directory |
| `find` | Search for files and directories |
| `-type f` | Search regular files |
| `-size` | Search using file size |
| `-user` | Identify file owner |
| `-group` | Identify group owner |
| `cat` | Display file contents |
| `grep` | Search for specific text |
| `sort` | Sort lines alphabetically |
| `uniq -u` | Display unique lines |
| `strings` | Extract readable strings |
| `2>/dev/null` | Hide error messages |
| `\|` | Connect commands using a pipe |

