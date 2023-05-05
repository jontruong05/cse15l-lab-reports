# Lab Report 3

This lab report will discover four alternate uses of the line command `grep` (`grep -c`, `grep -F, `grep -i`, and `grep -R`) on files and directories from `./technical`. 

## `grep -c`

`grep -c` is one of of the alternate uses of `grep`, and the command line takes the form `grep -c [key-word] [file-name]`. [key-word] is the string you would like to search for, and [file-name] is the name of the file you would like to search that string in. This alternate use of `grep` will display the number of times `[key-word]` appears in `[file-name]`. I've used the text file `chapter-1.txt` from the relative path `/technical/911report` as an example. Typing in the command `grep -c flight chapter-1.txt` prints out 74, as shown below:

![Image](grep-c.png)

