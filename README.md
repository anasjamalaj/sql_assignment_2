# sql_assignment_2
# Counting Organizations

## Description
This Python script is designed to solve the "Counting Organizations" SQL assignment. The goal of the assignment is to read the email data from a file named `mbox.txt`, count the number of email messages per organization (based on the domain name of the email address), and store these counts in a SQLite database table.

The script follows these steps:

1. **Read the mbox.txt file**: The script opens the `mbox.txt` file and reads its contents line by line. This file contains email data, including email addresses.

2. **Identify email domains**: The script defines a list of specific email domains (e.g., `iupui.edu`, `umich.edu`, `indiana.edu`, etc.) that need to be counted. It processes each line in the `mbox.txt` file and counts the occurrences of these domains.

3. **Store counts in a database**: The script creates a SQLite database file named `counts.db` and a table named `Counts` with two columns: `org` (TEXT) and `count` (INTEGER). It then inserts the counts of each email domain into the `Counts` table.

4. **Output the results**: After populating the database table, the script retrieves the counts from the `Counts` table, orders them in descending order based on the count value, and prints the expected output to the console. The output displays the email domains and their corresponding counts.

The script is designed to handle situations where it needs to be run multiple times or with different input files. Before each run, it truncates the `Counts` table by deleting all existing data, ensuring a fresh start for the new run.

The expected output from the script is:
Enter file name: mbox.txt

Counts:
iupui.edu 227
umich.edu 218
uct.ac.za 25
media.berkeley.edu 16
caret.cam.ac.uk 4
gmail.com 4
indiana.edu 0
vt.edu 0
ufp.pt 0
et.gatech.edu 0
