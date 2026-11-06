# OverTheWire Bandit – Levels 1 to 5

## Introduction

This journal documents my learning journey through OverTheWire Bandit Levels 1 to 5. Throughout these challenges, I practiced Linux commands, file navigation, reading files, identifying hidden files, and understanding file types.

## Learning Objectives

- Understand basic Linux commands.
- Navigate directories using the terminal.
- Read files with unusual filenames.
- Identify hidden files.
- Determine which files contain human-readable text.

---

## Level 1 → Level 2: Reading a File Named `-`

**Objective:** Read the contents of a file named `-`.

**Commands Used:**

```bash
ls
cat ./-
```

**Explanation:**
- `ls` displays files and directories.
- `cat ./-` reads the file named `-` in the current directory.

**What I Learned:**

I learned how to handle filenames that begin with special characters using a relative path.

---

## Level 2 → Level 3: Reading a File with Spaces

**Objective:** Read a file whose filename contains spaces.

**Commands Used:**

```bash
ls
cat "spaces in this filename"
```

**Explanation:**
- `ls` lists the available files.
- Quotation marks allow the terminal to interpret the filename with spaces as one argument.

**What I Learned:**

I learned how to work with filenames containing spaces by using quotation marks.

---

## Level 3 → Level 4: Finding Hidden Files

**Objective:** Locate a hidden file inside the `inhere` directory.

**Commands Used:**

```bash
cd inhere
ls -la
cat .hidden
```

**Explanation:**
- `cd inhere` enters the directory.
- `ls -la` displays all files, including hidden files.
- `cat .hidden` reads the hidden file.

**What I Learned:**

I learned that Linux hidden files usually begin with a dot (`.`), and `ls -la` can display them.

---

## Level 4 → Level 5: Identifying Human-Readable Files

**Objective:** Find the human-readable file among multiple files in the `inhere` directory.

**Commands Used:**

```bash
cd inhere
file ./*
```

Then read the file identified as human-readable:

```bash
cat ./FILENAME
```

**Explanation:**
- `cd inhere` enters the directory.
- `file ./*` identifies the type of each file.
- `cat` displays the contents of the correct file.

**What I Learned:**

I learned how to use the `file` command to identify file types and find readable text among multiple files.

---

## Overall Skills Developed

1. Linux terminal navigation.
2. File reading and handling.
3. Working with special characters and spaces.
4. Discovering hidden files.
5. Identifying file types.
6. Basic command-line problem-solving.

## Personal Reflection

Completing Bandit Levels 1–5 helped me become more comfortable using the Linux terminal. At first, some commands and filenames were confusing, but through practice and understanding each command, I became more confident in solving the challenges.

This experience strengthened my interest in Linux, cybersecurity, and ethical hacking. I look forward to continuing my journey through the next Bandit levels.

## Video Demonstration

Watch my practical demonstration of Bandit Levels 1–5:

[Bandit Level 1–5 Video](../videos/bandit-level-1-to-5.mp4)
