# Lab Report 5

## EdStem Post: Index Out Of Bound Exceptions with Command Line Arguments

Student: I'm trying to write a program that prints out at most 3 arguments from the command line when I run `java File`. However, I'm getting some `IndexOutOfBoundExceptions`. I think the problem may be with the for loop, but I'm not sure what the problem exactly is. 

Here are screenshots of my file structure, my Java source code called `File.java`, and a bash script called `script.sh`:

![Image](originalFile)

![Image](bashScript)

---

TA: The issue might not be the for loop itself, but rather a consideration you may be missing. What do you think happens when the lengths of `args[]` is small?

---

Student: Oh, I see the problem. It looks like the for loop is good at considering `args[]` of length 3 or more, but it's not great for when it's smaller than length 3. That's why I'm getting the `IndexOutOfBoundExceptions`. I've added an `if` statement to consider that case, along with code to process `args[]` when it has a length smaller than 3. I've also added some print statements for new lines to make the output look nicer: 

![Image](updatedFile)

## Setup Information

To recreate the debugging scenario in the pretend EdStem post above, you will need to create a new folder and then create a Java file and a bash script inside that folder. The names for the folder and files aren't too important, but in the case of the "student", you can name the folder `some-folder`, the Java file `File.java`, and the bash script `script.sh`. These file names will be used to refer to the folder, the Java file, and the bash script, respectively. 

The following should be in `File.java` to trigger the `IndexOutOfBoundExceptions`:

```
public class File {
  
  public static void main(String[] args) {
    for (int i = 0; i < 3; i++) {
      System.out.print(args[i] + " ");  
    }
  }
}
```

And the following should be in `script.sh`:

```
javac File.java
java File
java File Two words
java File Computer science seems pretty cool
```

The "TA" gave a hint that `args[]` of length smaller than 3 may have not been considered, which leads to the `IndexOutOfBoundsException` errors. To fix this, simply add an `if` statement before the `for` loop to check for the length of `args[]`. If it is less than 3, then it should be processed differently than if it were of length 3 or greater. Some print statements of newline characters were also added for the sake of making the output look neater. 
