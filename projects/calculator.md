---
layout: project
type: project
image: img/calc.jpg
title: "Stack-Based Calculator"
date: 2024
published: true
labels:
  - Java
summary: "A Stacked-Based Calculator I developed in ICS 211."
---

A stacked-based calculator I developed as an assignment in ICS 211, Spring 2024. In this program, I learned how to use stack data structures to process basic mathematical operations while also handling mathematical errors and syntax errors. 

This program had to be done in a week in [Eclipse](https://eclipseide.org/) using Java. A few key features that I now have an uderstanding of is <b>Push</b>, adding an item to the top of the stack, and <b>Pop</b>, removing and returning the item at the top of the stack. 

Here is an example code of how the Push and Pop methods were used the Stacked-Based Calculator:

```cpp
// iterate string arguments
for (String arg : args) {
// try to parse the argument as long
// push it onto the stack
	try {
		long number = Long.parseLong(arg);
		stack.push(number);
	} catch (NumberFormatException e) {
		// check if there are fewer than 2 numbers on if the argument is not a number
		if (stack.size() < 2) {
		// append "syntax error" to the result
		result.append("syntax error\n");
		// continue to the next argument
		continue;
		}

// pop the top two numbers from the stack to apply the operator
long secondOperand = stack.pop();
long firstOperand = stack.pop();

//code continues
	}
}
```
