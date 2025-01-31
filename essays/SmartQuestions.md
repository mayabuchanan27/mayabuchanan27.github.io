---
layout: essay
type: essay
title: "Smart Questions, Good Answers"
# All dates must be YYYY-MM-DD format!
date: 2024-01-30
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## Is there such thing as a stupid question?

The best way for software engineers to gain experience is to practice problem solving. This can be done by debugging code, engaging in new frameworks, or simply finding online coding challenges. However, no matter how skilled an engineer is, they will most likely encounter frustrating problems that require online help. It is quite common for engineers to turn to online resources, such as Stackoverflow, when an issue is presented to them. 

Stack Overflow is one of the largest and most active programming communities, where developers can ask and answer technical questions. But, not all questions are created equal. Some receive immediate, high-quality responses, while others are ignored, shot down, or even deleted. The difference is often determined by the structure of the question.

## What’s a smart question?

An example of a “smart” question would be the following case, where a user is asking for a simple way to print an array in Java after he/she ecounters a problem in printing their array. 

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

While the heading of his question could be better, it does convey what he’s trying to figure out. Usually something as brief as “python date of previous month” is what other users would enter in as search terms on Google, making it easily found. Another good thing about the question is that it’s not just a question. The asker shows what he or she has done and that he or she has put in some effort to answer the question. And while it may not be as important as the question itself, the asker shows courtesy, which does increase the chance of getting an answer.

```
A: datetime and the datetime.timedelta classes are your friend.

1. find today
2. use that to find the first day of this month.
3. use timedelta to backup a single day, to the last day of the previous month.
4. print the YYYYMM string you're looking for.

Like this:

 >>> import datetime
 >>> today = datetime.date.today()
 >>> first = datetime.date(day=1, month=today.month, year=today.year)
 >>> lastMonth = first - datetime.timedelta(days=1)
 >>> print lastMonth.strftime("%Y%m")
 201202
 >>>

```
 
The asker received six possible answers, and he or she was successful in inciting discussion from multiple users. The answers themselves were clear and were devoid of the rumored sarcasm and hostility of “hackers.” Since I myself have referenced this page and found it useful, I can confidently say that it is a good question.

## The foolproof way to get ignored.

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.
