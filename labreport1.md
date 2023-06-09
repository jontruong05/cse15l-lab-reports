# Lab Report 1

This lab report will demonstrate how to set up remote access by logging into a course-specific account on `ieng6`, particularly for CSE 15L.  

## Installing VSCode

First, you will need to download Visual Studio Code (VSCode). Click [here](https://code.visualstudio.com/download) to go to the download site for VSCode. Be sure to download the one that corresponds with your operating system.

Here's what it should look like if you are on a Mac:  

![Image](step1.png)

Click on the downloaded zip folder. It should take you to your downloaded folders, where you will see an application named "Visual Studio Code". Open it up, and it should look something like this upon startup:  

![Image](step2.png)

## Remotely Connecting

Click on "Terminal" on the top left bar, and then click "New Terminal". Inside the terminal, type `ssh [your-cse15l-username]@ieng6.ucsd.edu`, where `[your-cse15l-username]` should be replaced with your CSE 15L username. The terminal will prompt you to enter your password. Be sure to type it in carefully, as you will not be able to see what you are typing. 

Once you've typed in your password, hit Enter. Your terminal should look something like this:  

![Image](step3.png)

## Trying Some Commands

At this point, we can start typing in some commands in the command line. The four examples shown in the screenshot below are as follows:
* `ls`, which prints out all items in the current directory. In this case, there's a file called "perl5". 
* `pwd`, which prints out the absolute file path on the remote computer. 
* `cat /home/linux/ieng6/cs15lsp23/public/hello.txt`, which attempts to print out the contents from a text file called "hello.txt". Unfortunately, the terminal is saying that "hello.txt" doesn't exist.
* `ls -a`, which prints out all files, including ones that start with ".". 

![Image](step4.png)

Fantastic! You are now able to set up remote access to a computer in the CSE basement and run some commands. 
