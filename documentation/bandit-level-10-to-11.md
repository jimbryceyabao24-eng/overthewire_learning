OverTheWire Bandit Level 10 → Level 11

Learning Objectives

After completing this challenge, I learned how to:

Understand what Base64 encoding is and why it is used to represent data.

Identify encoded text stored inside a file using Linux commands.

Use the cat command to read the contents of a file.

Use the base64 -d command to decode Base64-encoded data.

Understand the purpose of the -d option, which means decode.

Retrieve a password from an encoded text file.

Use the decoded password to access the next Bandit level through SSH.

Commands Learned

Command

Description

ls

Lists files and directories.

cat data.txt

Displays the contents of a file.

base64 -d data.txt

Decodes Base64-encoded content.

ssh

Connects to a remote server securely.

Steps Performed

1. Log in to Bandit Level 10

ssh bandit10@bandit.labs.overthewire.org -p 2220

2. Check the available file

ls

The file provided in this level is data.txt.

3. Read the encoded content

cat data.txt

The output contains a Base64-encoded string.

4. Decode the content

base64 -d data.txt

The command decodes the Base64 text and displays the password for Bandit Level 11.