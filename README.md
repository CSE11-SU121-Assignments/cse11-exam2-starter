# Exam 2

This page details a **take-home exam** that you will complete over the next
few days. You can't communicate with anyone about the content of the
assignment until you receive your grade. The course staff will not give
debugging advice or answer questions about the problems. If you have
technical trouble creating a screencast (detailed below) feel free to reach
out for assistance.

You **can** make use of any course notes, online resources, Java tools, and
so on to complete the exam.

You will complete the programming tasks 1 and 2 in the file `ArrayExamples.java` in the `ArrayExamples` class. Task 3 should be implemented by adding to the file `ExamplesSearch.java`. You should submit both files `ArrayExamples.java` and `ExamplesSearch.java` to the `Exam2` Gradescope assignment.

You will also submit a **video screencast** of yourself presenting a portion of it to this [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSd00Y2y2kggLCyIKsAEIWiqw-ZwZt1caMkLma1phZKB3N96lQ/viewform?usp=sf_link).

Submission checklist (see long descriptions below for full details):

- `[ ]` `findSecond` method in the `ArrayExamples` class
- `[ ]` `findNth` method in the `ArrayExamples` class
- `[ ]` A comment describing the `mystery` method in `ArrayExamples`
- `[ ]` A test for the `mystery` method in `ArrayExamples` that threw an exception in the original implementation of that method
- `[ ]` Modified the `mystery` method to not throw exceptions
- `[ ]` `AllQuery` class
- `[ ]` Constructed three instances of `AllQuery` with specified array lengths
- `[ ]` Six tests using these constructed `AllQuery` objects
- `[ ]` Screencast
  - Picture ID + Face
  - Trace evaluation of the `AllQuery` test


Your submission will be graded **after** the deadline. The Gradescope upload
will just check to make sure that there aren't any errors reported by Java
when we try to run your programs, not whether tests succeeded or failed. You
should test thoroughly yourself to make sure your program works as expected.

## Tasks

Download the starter code. Some of the starter code is very lightly adapted from [this reading](https://cseweb.ucsd.edu/classes/sp17/cse11-a/lecture11.html).

(The `ExamplesSearch` class is identical to the start code from Exam 1)

You should **not** change any of the existing methods or classes except for the `mystery` method, and adding to `ArrayExamples` and `ExamplesSearch`. Don't change `ImageQuery` or the other query classes, just add new ones as described below.

Also, ensure that the methods take arguments in the same order that is mentioned in the tasks. Mixing up the order makes it more difficult to grade and can also prevent you getting any feedback from Gradescope's autograder.

### Task 1

1. Add a **method** to the `ArrayExamples` class called `findSecond` that takes a `String[]` and a `String` and returns the _index of the second time_ that string appears in the array, or `-1` if it appears in the array 1 or 0 times. For example, for the array input `{"a", "b", "a", "a"}` and

   - the string input `"a"`, it should produce 2.
   - the string input `"b"`, it should produce -1.
   - the string input `"c"`, it should produce -1.

2. Add another method to the `ArrayExamples` class called `findNth` that takes a `String[]`, a `String`, and an `int` `n`. It should behave the same as `findSecond`, but look for the _index of the `n`th time_ the string appears in the array. For example, for the array input `{"a", "b", "a", "a"}`

   - the string input `"a"`, and int `2`, it should produce 2.
   - the string input `"a"`, and int `3`, it should produce 3.
   - the string input `"a"`, and int `4`, it should produce -1.
   - the string input `"b"`, and int `2`, it should produce -1.
   - the string input `"c"`, and int `2`, it should produce -1.

You can assume that all inputs to both of these methods are not `null`, and `n` is always greater than 0. You are not required to write tests for these methods, though as always we encourage you to do so.

### Task 2

1. Consider the `mystery` method in the `ArrayExamples` class. Write a comment above this method describing what it does in a *single* English sentence.
2. Write a test for `mystery` which calls it with an input **other than** `null` for `nums` which causes an exception when run. Write this test as a field named `taskTwoTest` in `ArrayExamples`.
3. Change the `mystery` method so that **no inputs** can cause an exception to be thrown, and the method instead returns an empty array for the inputs that caused exceptions on the original version. Note that you must _modify_ this method, not write a new method. You may only use Java constructs we have learned in this class, and you must ensure that mystery's behavior does not change on valid inputs. You can always go back to the web page for the starter code to see the original version if you make edits and want to see the original again.

### Task 3

1. In the file `ExamplesSearch.java`, add a new class called `AllQuery` implementing `ImageQuery`. It should have a field of type `ImageQuery[]` and a corresponding constructor to initialize that field. Its `matches` method should return `true` when _all_ of the queries in the list match the given image. If the query array is empty, `matches` should return `true` for any `ImageData`.

2. Create three `AllQuery` objects with arrays of size 1, 3 and 5, each containing different queries. Demonstrate using each query's `matches` method on at least two different `ImageData` inputs, once returning `true` and once returning `false`. So at least 6 tests in total. (You can and should write _more_ tests than this to ensure that the class works as you expect, but this is what we'll check for).

### Task 4 – Video

You will record a short video of no more than 5 minutes. Include:

- Show only your face and a picture ID (your student ID is preferred) for a few seconds at the beginning. You don't
  have to be on camera the whole time, though it's fine if you are. Just a
  brief confirmation that it's you creating the video/doing the work attached
  to the work itself is what we want.
- For the `AllQuery` with array of size 3 that you created in [Task 3](#task-3):

  Run the `ExamplesSearch` program and show the output corresponding to a method call for this example. Then, starting from the line in your code with the call to the `matches` method, indicate each line of code that runs in your program while evaluating that method call. You can scroll to and click the lines to highlight them, or otherwise indicate each one. You should indicate them in the order that **Java will evaluate them** (this might be different than the order they appear in the file).

An example of what your video should look like when doing this kind of
explanation is here:

[https://drive.google.com/open?id=1E-TcVXSg9BI4MnWoVU9_BbcRJsu8ZhCf](https://drive.google.com/open?id=1E-TcVXSg9BI4MnWoVU9_BbcRJsu8ZhCf)

PA5 has a tutorial for creating a screencast like this
[https://github.com/CSE11-SP21-Assignments/cse11-sp21-pa5-starter](https://github.com/CSE11-SP21-Assignments/cse11-sp21-pa5-starter).

Here are some notes from the graders on how to improve your videos:

- Make sure to use a picture ID, either a driver's license or passport that has a picture of you. If you do not provide a picture ID, you will get a 0 on the exam until prove to us it was you who did the video.
- Make sure your picture ID and face are visible at the same time for three or four seconds. We must be able to pause the video and verify it's you. Again, if we can't verify it's you, you will get a 0 on the exam until prove to us it was you who did the video. Make sure to fill up the screen as much as possible with your face and picture id (i.e. don't stand far away from your camera).
- When you start recording your video, start with screen share off and camera on and show your picture ID and face (close-up!!). Then you can enable screen share (and disable camera) and walk through your code.
- Video must have sound! While highlighting your code, also make sure to explain the code. We must hear you explain it!
- Once you enable screen share, make sure to leave it on the entire time while explaining your code.
- Do not explain every test case! Only explain what you are explicitly told in the write-up.
- Keep your videos under 5 minutes. We will penalize all students who go over 5 minutes. To ensure you stay under 5 minutes, make sure to only explain the test cases that the write-up says you should. Do not explain extra code that is not requested by the write-up.
