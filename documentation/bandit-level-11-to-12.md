Bandit Level 11 → Level 12

Objective

Find the password for the next level. The password is stored in data.txt, which contains text encoded using ROT13.

Commands Used

ls
cat data.txt
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

Explanation

ls - Lists the files in the current directory.

cat data.txt - Displays the contents of the file.

tr 'A-Za-z' 'N-ZA-Mn-za-m' - Decodes the ROT13-encoded text.

What I Learned

ROT13 is a letter substitution cipher.

The tr command can translate characters.

ROT13 uses the same process for encoding and decoding.

A pipe (|) allows the output of one command to become the input of another command.