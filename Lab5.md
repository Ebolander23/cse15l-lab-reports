# Lab Report 5 - Debugging Scenario
# Eric Bolander
# Dr. Politz

### Title: Test Failures TestDocSearch 

Student Post:
Hey Everyone, I am trying to run my test script for TestDocSearch and am getting the output below.

![Image](test.sh.png)

I am pretty sure that I wrote my script correctly, however it seems to be something wrong with the tests themselves?
Here are the tests for DocSearch in the TestDocSearch class:

![Image](TESTS.png)

Here are the error messages I am gettting back:
![Image](fail.png)


Here is the test.sh class:

![Image](test.sh.png)


```
TA Response:
Hello! Thank you for sharing the details of the bug you are encountering.
It looks as if the java file you have downloaded is actually a linux file.
The issue stems from where you are running your tests. 
A question to think about: What are the differences in how to write paths between Linux and Windows?
```

```
Student Response:
Thank you! So the error that I am getting is due to the different slashes associated with the Linux system, 
does that mean I have to completely rewrite all the code within the testing class?
```

```
TA Response:
Yes, you are definitely on the right track. When you are thinking about these kind of bugs,
it is also important to think about where you are running your code.
Do you think you would get the same error if you tried logging into a remote server?
Try running these commands again, but try using the ssh command to log into IENG first.
```
Student Response:
Thank you! It worked, and now my tests work! Thank you.
Tests Working:
![Image](testworking.png)
Server Running:
![Image](search.png)

# Contents of the Directory and files within: 
![Image](directory.png)
![Image](start.sh.png)
![Image](TestDocSearch.png)


# Part 2: Reflection
```
I really enjoyed learning and using vim. It is not only useful to make quick changes from the terminal,
but creating new files, and navigating big code. 
I think another topic that we covered in class that I enjoyed was learning about scripts
and running those from the terminal.
Not only is writing a script really useful, but it also unlocks much more efficient coding and testing.
I am going to make scripts a part of my coding, and it was nice to get lots of practice during lab
running and testing our code using scripts.

```
