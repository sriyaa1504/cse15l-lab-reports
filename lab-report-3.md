# Lab Report 1
---
## Topic : Researching Commands
---
### The command I will be choosing for this lab report is `-grep`
---

> COMMAND 1 `-r`
**SOURCE: ChatGPT**
```
EXAMPLE 1 
Command: [cs15lwi23ain@ieng6-202]:skill-demo1-data:400$ grep -r "Hello" .

Output:
./written_2/non-fiction/OUP/Berk/CH4.txt:Children’s earliest efforts at make-believe also reveal how challenging they ﬁnd the task of detaching thought from reality. Initially, object substitutions are closely tied to the real things they represent. Toddlers between ages 1 1/2 and 2 generally use only realistic-looking objects while pretending—a toy telephone to talk into or a cup to drink from.9 Once, I handed a 21-month-old a small wooden block, put another to my ear, and called her on the phone: “Ring! Ring! Hello, Lynnay!” She responded by throwing down the block and turning to another activity. Yet when given a plastic replica of a push-button phone, Lynnay readily put the receiver to her ear and pretended to converse.
./written_2/non-fiction/OUP/Berk/CH4.txt:As children engage in play talk, they not only build their vocabularies but correct one another’s errors, either directly or by demonstrating the acceptable way to speak. In one instance, a kindergartner enacting a telephone conversation said, “Hello, come to my house, please.” Her play partner quickly countered with appropriate telephone greeting behavior: “No, ﬁrst you’ve got to say ‘How are you? What are you doing?’”28
./written_2/travel_guides/berlitz1/WhereToFrance.txt:        Saint-Wandrille, Le Bec-Hellouin, and Caen, culminating in their
```
- This command uses `-r` to recursively search through all the files in the directory.
- It returns all occurences of the word "Hello".
- It is beneficial when we want to search for a specific word in all the files present.

```
EXAMPLE 2
Command: [cs15lwi23ain@ieng6-202]:skill-demo1-data:401$ grep -r --exclude-dir=non-fiction "Hello" .

Output:
./written_2/travel_guides/berlitz1/WhereToFrance.txt:        Saint-Wandrille, Le Bec-Hellouin, and Caen, culminating in their
```
- This command uses `--exclude-dir=` to exclude a directory while searching for a pattern.
- The `.` searches through all the files present.
- This command can be useful when there a lot of directories and we want to ignore only a specific one.


> COMMAND 2 `-c`
**SOURCE: ChatGPT**
```
EXAMPLE 1
Command:
[cs15lwi23ain@ieng6-202]:Berk:411$ grep -c "Hello" CH4.txt

Output:
2
```
- This command uses `-c` to count the number of occurrences of a pattern in a file.
- This can be useful when the file is huge.

```
EXAMPLE 2
Command:
[cs15lwi23ain@ieng6-202]:Berk:412$ grep -v -c "Hello" CH4.txt

Output:
311
```
- This command uses `-v` to count the number of lines in a file that do not match a pattern.
- It helps when there are many lines in a file and the pattern occurs only a few times.


> COMMAND 3 `-i`
**SOURCE: ChatGPT**
```
EXAMPLE 1
Command:
[cs15lwi23ain@ieng6-203]:Berk:390$ grep -i "hello" CH4.txt

Output:
Children’s earliest efforts at make-believe also reveal how challenging they ﬁnd the task of detaching thought from reality. Initially, object substitutions are closely tied to the real things they represent. Toddlers between ages 1 1/2 and 2 generally use only realistic-looking objects while pretending—a toy telephone to talk into or a cup to drink from.9 Once, I handed a 21-month-old a small wooden block, put another to my ear, and called her on the phone: “Ring! Ring! Hello, Lynnay!” She responded by throwing down the block and turning to another activity. Yet when given a plastic replica of a push-button phone, Lynnay readily put the receiver to her ear and pretended to converse.
As children engage in play talk, they not only build their vocabularies but correct one another’s errors, either directly or by demonstrating the acceptable way to speak. In one instance, a kindergartner enacting a telephone conversation said, “Hello, come to my house, please.” Her play partner quickly countered with appropriate telephone greeting behavior: “No, ﬁrst you’ve got to say ‘How are you? What are you doing?’”28
```
- The `-i` command allows you to perform a case-insensitive search for a pattern in a file.
- This is useful when the word is present in both uppercase and lowercase.
```
EXAMPLE 2
Command:
[cs15lwi23ain@ieng6-202]:Berk:413$ grep -i "hello" ch2.txt ch7.txt ch1.txt

Output:

```
- The `-i` command can also be performed on multiple files at once which saves time and labor.
- Since there are no occurences of "hello" in any of those files, the output is empty.

> COMMAND 4 `-A`
**SOURCE: ChatGPT**
```
Command:
