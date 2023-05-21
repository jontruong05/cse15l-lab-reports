# Lab Report 4

This lab report will execute the following steps of CSE 15L's Week 7 Lab Activity. These steps are:
1. Log into ieng6
2. Clone your fork of the repository from your Github account
3. Run the tests, demonstrating that they fail
4. Edit the code file to fix the failing test
5. Run the tests, demonstrating that they now succeed
6. Commit and push the resulting change to your Github account (you can pick any commit message!)

## Step 1

First, we will log into the `ieng6` account. Note that this time, the terminal isn't prompting the user to enter the password-that's because an SSH key has been created for the `ieng6` account so that we no longer have to enter in the password. Sweet! 

![Image](ieng6login.png)

Keys pressed: ssh<space>cs15lsp23qq<shift-2>ieng6.ucsd.edu<enter>

## Step 2

Now that we're logged in, let's clone this repository on GitHub: https://github.com/ucsd-cse15l-s23/lab7.git

![Image](gitclonelab7.png)

Keys pressed: git<space>clone<space><cmd+v><enter>ls<enter> (<cmd+v> refers to pasting the link to the GitHub repository, so be sure to copy the link first and then pasting it into the terminal)

## Step 3
  
Now, we must show that by running the tests in the `.java` files, we get failures. First, we must get into the `lab7` directory:
  
![Image](cdlab7pwdls.png)
  
Keys pressed: cd<space>lab7<enter>pwd<enter>ls<enter>
  
Next, we will compile `ListExamples.java` and `ListExamplesTests.java` simultaneously using the `javac` command:

![Image](compile.png)

Keys pressed: javac<space><cmd+v><space><shift+8>.java<enter>ls<enter> (<cmd+v> refers to pasting this: -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar)

And finally, we show that there are errors in the tests using the `java` command:

![Image](failure.png)

Keys pressed: java<space><cmd+v><space><shift+l>ist<shift+e>xamples<shift+t>ests<enter> (<cmd+v> refers to pasting this: -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore)

## Step 4

Not to worry, we can fix the issue by editing the file directly from the terminal! It turns out that the issue is in the `ListExamples.java` file. To get into that file, first type "vim ListExamples.java":

![Image](vim_command.png)

After pressing enter, this is what the terminal should look like:
  
![Image](editListExamples.png)
  
Keys pressed: vim<space><shift+l>ist<shift+e>xamples.java<enter>
