---
layout: project
type: project
image: img/book.jpg
title: "Binary Search Tree for String Analysis"
date: 2024
published: true
labels:
  - Java
summary: "Analyzing string data using a binary search tree that I developed in ICS 211."
---

I developed this string analysis program that uses a <b>binary search tree</b> as an assignment in ICS 211, Spring 2024. From this program, I learned how to use a binary search tree to read strings from a file and track the occurrence of each unique word, which ultimately is useful to efficently organize data.

This program had to be done in a week in [Eclipse](https://eclipseide.org/) using Java. The most challenging part of this program was figuring out how to traverse about in the binary search tree. Despite the challenges I faced while writing this program, I gained an understanding of how to traverse a binary search tree using recursive methods, such as in-order traversal to retrieve all unique words in sorted order and other methods for searching, counting, and calculating tree properties. 

Below are examples of key recursive methods that demonstrate the functionality of the program:

<b>Adding Nodes:</b> A method that shows how the program recursively builds the binary search tree by traversing the tree to find the correct position for a new node or increment the value if the key already exists:
```cpp
// recursive method
private BinaryNode addKey(String key, BinaryNode node) {
  // convert string to lowercase
  String keyLower = key.toLowerCase();

  // new node is created when node is null (base case)
  if (node == null) {
    return new BinaryNode(key);
  }
  // compare lowercase key with current node (converted to lowercase)
  int cmp = keyLower.compareTo(node.key.toLowerCase());

  // if smaller go left
  if (cmp < 0) {
    node.left = addKey(key, node.left);
  // if bigger go right
  } else if (cmp > 0) {
      node.right = addKey(key, node.right);
  // if equal, it is in the tree, increment count
  } else {
    node.value++;
  }
  return node;
}

<b>Retrieving Key:</b> A method how recursion is used to traverse the tree to retrieve a specific key:
```cpp
// recursive method
private long findOccurrences(String key, BinaryNode node) {
  // key not found when node is null (base case)
  if (node == null) {
    return 0;
  }

  // compare key with key of current node
  int cmp = key.compareTo(node.key.toLowerCase());

  // if key is less than node's key, search left subtree
  if (cmp < 0) {
    return findOccurrences(key, node.left);
  // if key is greater than node's key, search right subtree
  } else if (cmp > 0) {
    return findOccurrences(key, node.right);
  // if keys are equal, return occurences count of the current node
  } else {
    return node.value;
  }
}
```
<b>Calculating Height:</b> A method that shows how recursion can be used to compare paths in a tree by calculating its the height:
```cpp
// recursive method
private int calculateHeight(BinaryNode node) {
  // tree is empty if node is null, return 0
  if (node == null) {
    return 0;
  }

  // calculate height of left and right subtrees
  // return greater height and add 1 for current node level
  return 1 + Math.max(calculateHeight(node.left), calculateHeight(node.right));
}
```
