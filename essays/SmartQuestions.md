---
layout: essay
type: essay
title: "Smart Questions, Good Answers"
# All dates must be YYYY-MM-DD format!
date: 2025-01-30
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded d-block mx-auto" src="../img/questions.jpg">

## What's the Point in Asking?

The best way for software engineers to gain experience is to practice problem solving. This can be done by debugging code, engaging in new frameworks, or simply finding online coding challenges. However, no matter how skilled an engineer is, they will most likely encounter frustrating problems that require online help. It is quite common for engineers to turn to online resources, such as Stackoverflow, when an issue is presented to them. 

Stack Overflow is one of the largest and most active programming communities, where developers can ask and answer technical questions. But, not all questions are created equal. Some receive immediate, high-quality responses, while others are ignored, shot down, or even deleted. The difference is often determined by the structure of the question.

## What’s the "Smart" Structure?

An example of a “smart” question would be the following case, where a user is asking for a simple way to print an array in Java after they ecounter a problem in printing their array. 

Q:[What's the simplest way to print a Java array?](https://stackoverflow.com/questions/409784/whats-the-simplest-way-to-print-a-java-array)
```
In Java, arrays don't override toString(), so if you try to print one directly, you get the className + '@' + the hex of the hashCode of the array, as defined by Object.toString():

int[] intArray = new int[] {1, 2, 3, 4, 5};
System.out.println(intArray); // Prints something like '[I@3343c8b3'
But usually, we'd actually want something more like [1, 2, 3, 4, 5]. What's the simplest way of doing that? Here are some example inputs and outputs:

// Array of primitives:
int[] intArray = new int[] {1, 2, 3, 4, 5};
// Output: [1, 2, 3, 4, 5]

// Array of object references:
String[] strArray = new String[] {"John", "Mary", "Bob"};
// Output: [John, Mary, Bob]
```
This demonstrates a "smart" question since the user is able to clearly provide a question, which includes example code that brought upon the issue. Additionally, they demonstrate prior understanding by acknowledging that Java does not override toString() for arrays and specifically ask for the simplest solution rather than a less direct solution. This structured example approach makes it easy for the community to provide straightforward and helpful answers.

## Avoid Being Unclear
An example of an unclear question would be the following case, where the user is asking for help to properly display text while using the RoundedBorder in a Java Swing program.

Q: [Test is not displaying in button created using JButton in Java swing](https://stackoverflow.com/questions/79401775/test-is-not-displaying-in-button-created-using-jbutton-in-java-swing)
```
When I add a RoudedBoder class to add curved Boder in button in java swing the text got disappeared just showing 3dots. I changed the size of the text and decreases radius of the border but no using. The text is visible only when the radius of the border become 0

I need to make the text inside the button visible without removing RoundedBorder
```

This demonstrates a unclear question due to the user's vague description of their problem. Furthermore, the heading for this post is not a question, rather it is the problem that the user is struggling with. Besides the poor grammar and no clear question being asked, the user also fails to provide code, which results in the community not being able to examine the issue properly to give feedback. Without making improvements, this user's post will probably not receive answers due to the lack of information.  

## Conclusion
The quality of a question often determines the quality of the answer it receives. A well-structured question with clear context, example code, and a specific goal is the type of questions we want to ask in order to get a helpful response. Whereas short questions with unclear information will most likely not be answered. By taking the time to ask smart questions on websites, like Stack Overflow, developers can get better answers to acheive their goal of learning more effectively.
