---
layout: post
title: Understanding Pseudo-Code
---


Pseudo code, is meant for humans to read and not meant
for machines or programs to process. Therefore, there
is no rigid format to follow.

Here's an example of some pseudo-code for a method that determines which number is greatest in a collection:

```
Given a collection of integers.

Iterate through the collection one by one.
  - save the first value as the starting value.
  - for each iteration, compare the saved value with 
    the current value
  - if the saved value is greater, or it's the same
    - move to the next value in the collection
  - otherwise, is the current value is greater
    - reassign the saved value as the current value

After iterating through the collection, return the saved value.
```

Now with the pseudo-code above we try to absorb the problem and load it into our brain first.

⋅⋅* Spend time absorbing the problem, this may require you to diagnose the problem time and time again in your head

⋅⋅* Once you've absorbed the content you can start to dissect it, understand it, and come up with an execution path to solve it

⋅⋅* Using pseudo-code helps us focus on the logical problem domain layer without dragging us into getting caught up with syntactical issues such as mistyped errors and typos, etc. Also known as programming language syntax issues

Before translating our pseudo-code into real code we "formalize" the pseudo-code a little more. By that I mean, we use some keywords to help us break down the program logic into concrete commands, which will then make translating to real code much easier. The keywords are:


#### Keywords and Meaning
![keywords-meaning](/images/keywords_meaning.png){:class="img-responsive"}


Using the keywords above to act as pseudo programming syntax, but still written in English it adds more structure to the pseudo-code and to let us think at a more detailed level. Here is the translation:

```
START

# Given a collection of integers called "numbers"

SET iterator to = 1
SET saved_number = value within numbers collection at space 1

WHILE iterator <= length of numbers
  SET current_number = value within  numbers collection at space "iterator"
  IF saved_number >= current_number
    go to the next iteration
  ELSE
    saved_number = current_number

  iterator = iterator + 1

PRINT saved_number

END
```

This approach from going to pseudo-code to a more formalized revised version of pseudo-code allows us to now worry about the programming language syntax. Now we need to test the logic by translating it into program code.





Now that you have an image to reference, let's begin. I am going to layout this process in order using a numbered list.

1. Read through the code or question and digest the problem thoroughly.
2. Identify the inputs and outputs for the problem.
3. Define the inputs and outputs values if possible.
4. Write down any implicit requirements.
5. Determine where there needs to be clarifying questions.
6. Come up w/ a mental model to describe it.
7. Come up with Examples/Test Cases
8. Determine what data structures we'll work with to convert the input to output
9. Get the right level of detail to readily convert to code without actually writing code


<!-- Link syntax reference
[Jekyll Now repository](https://github.com/barryclark/jekyll-now) -->