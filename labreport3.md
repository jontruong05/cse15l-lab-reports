# Lab Report 3

This lab report will discover four alternate uses of the line command `grep` (`grep -c`, `grep -F, `grep -i`, and `grep -R`) on files and directories from `./technical`. 

## `grep -c`

`grep -c` is one of of the alternate uses of `grep`, and the command line takes the form `grep -c [key-word] [file-name]`. [key-word] is the string you would like to search for, and [file-name] is the name of the file you would like to search that string in. This alternate use of `grep` will display the number of times `[key-word]` appears in `[file-name]`. I've used the text file `chapter-1.txt` from the relative path `/technical/911report` as an example. Typing in the command `grep -c flight chapter-1.txt` prints out 74, as shown below:

![Image](grep-c.png)

This shows that the word `flight` appears 74 times in the text file `chapter-1.txt`. 

## `grep -F`

`grep -F` is a `grep` alternate that prints out all the lines in a certain file that contains a specified keyword. This command takes the form `grep -F [key-word] [file-name]`. As an example, I switched to the `biomed` directory in `technical` and typed in the command `grep -F polar 1471-2148-1-14.txt`. Here was the result of the command: 

![Image](grep-F.png)

The command searched throughout `1471-2148-1-14.txt` and determined that there were two lines that contained the word `polar`. So as a result, two lines from that text file were printed. 

## `grep -i`

`grep -i` is a `grep` alternate that searches through a text file for a particular keyword, but ignores case sensitivity. Recycling our last example, the command `grep -i POLAR 1471-2148-1-14.txt` will have the same output as `grep -F polar 1471-2148-1-14.txt` as shown below:

![Image](grep-i.png)

So even though the keyword is `POLAR`, lines that contain `polar` are still printed.

## grep -R

`grep -R` is a `grep` alternate that searches through the current directory and its subdirectories for files that contain a specified keyword. It takes the form `grep -R [key-word] .`. After switching the current directory to `technical`, I typed the command `grep -R "genome sequencing" .` and got: 

![Image](grep-R.png)

The command lists out the relative paths of the files that contain the keyword "genome sequencing" and prints out the lines that contain "genome sequencing". 

## Linked Used

The following is the link I used to discover alternates of the `grep` command: https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/ 
