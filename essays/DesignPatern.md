---
layout: essay
type: essay
title: "The Habit of Coding Standards"
# All dates must be YYYY-MM-DD format!
date: 2025-05-04
published: true
labels:
  - Design Patterns
---

<img width="640" height="300" class="rounded float-start pe-4" src="../img/blueprint.avif">

## The Balance of Functionality and Readability 
Imagine having all the materials to build a house except for a blueprint. That’s how software feels without design patterns: fragile, inconsistent, and hard to scale. Design patterns are reusable solutions to common programming problems, much like architectural plans that guide the structure of a building. They help developers organize code, avoid repetition, and communicate ideas more clearly.

## My experience
In the six-part Digits assignment, I learned about the Factory pattern. I used it to return the correct React component depending on the type of digit being displayed. Instead of writing long chains of conditional logic, I created a single function that took a digit type and returned either the edit, add, admin, etc. component. It made the code much easier to read, maintain, and extend later into the later parts of the assignment.
