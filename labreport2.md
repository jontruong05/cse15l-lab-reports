# Lab Report 2

This lab report consists of three parts. Part 1 will discuss the implemetation of a web server named `StringServer`. Part 2 will discuss the method testing of `reverseInPlace()` in the `ArrayExamples.java` file. Part 3 will discuss what I learned during week 2/3 of CSE 15L that I did not know before. 

## Part 1

The implementation of the `StringServer.java` file looks like this: 

![Image](StringServer source code.png)

When a server request takes the form `/add-message?s=<string>`, the string that follows the `=` will be added to an ArrayList of strings. The page will also display a message "Value added!" to signal that a string has been added to the ArrayList. 

The following two screenshots will demonstrate this type of request in action. The follow screenshot corresponds to `/add-message?s=Hello`:

![Image](:add-message?s=Hello.png)

And this following screenshot corresponds to `/add-message?s=How are you`:

![Image](:add-message?s=How are you.png)

For the previous two requests, the `handleRequest()` method is called upon in the `Handler` class. It takes a `URI` as the argument, which contains the path and query of the request. The if statement in the `handleRequest()` method checks for the contents in the path and the query--if the path has `/add-message` and the query has `s=`, then the server will proceed to add the string that follows the `s=` to the ArrayList named `strList`. 

The else statement runs for any other values of the path or query. What happens is that there is a for loop that will iterate through `strList` and concatenate each element in it with a new line to an empty String named `str`. Note that `str` is only available within the else statement. Once the for loop finishes iterating through `strList`, `str` will be printed onto the page. 

At this point, the `StringServer` page should show:

![Image](StringServer page.png)

## Part 2

We will observe the method testing of `reverseInPlace()` in `ArrayExamples.java`. The following code snippet is a test method for `reverseInPlace()`:

`
@Test
  public void testOtherReverseInPlace() {
    int[] intArr = {1, 2, 3, 4, 5};
    ArrayExamples.reverseInPlace(intArr);
    assertArrayEquals(new int[] {5, 4, 3, 2, 1}, intArr);
  }
`

## Part 3
