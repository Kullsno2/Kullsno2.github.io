---
layout: post
title: How to Recursion
categories: blog
tags: ['recursion','algorithm','lollu sabha']
excerpt: 'Everything you need to know about recursion'
date: June 10, 2018
author: self
image:
    feature: how-to-recursion/comic.jpg

---

In this blog post I will shed light upon the basic concepts of
recursion and its application in various algorithmic problems.

**Disclaimer: I am not a subject expert on recursion and I am
sharing my findings as I learn more about this myself.**

Prerequisites:

1. A decent Internet connection with an upload speed of 2.75 Bits Per Second xD
2. Read the first requirement again.

## What is Recursion

You may have heard this word again and again when you were learning the
concepts of Linked lists and Binary trees. Recursion is one of the powerful
features of a programming language which accomplishes much more than the
iterative algorithms.Before we dive deep into the recursion concepts and recur
ourselves,read [this](https://www.geeksforgeeks.org/recursion/) article on
geeksforgeeks which gives a head start to those who are unaware of the word recursion.

## Concept

The basic concept of recursion is as simple as that. The initial call to the recursive
function has the initial arguments and makes the call. The calls keep on going until
the target man is reached. When the target man gets the call , he does some calculations
or whatever and returns the result back to the caller.

## Proposal scenario

Consider the following fruitful scenario.Mythili has a crush on Akshay.She decides 14th of
February as the auspicious day to propose her love to Akshay. She feels shy , so she comes
up with a plan which would make her more comfortable.There are about 8 people standing
in between Mythili and Akshay. As the teacher has entered the class she cannot shout out to
Akshay and say "Akshay, Yessu Paraaah Akshayyy".So she types out the following snippet and passes it to her neighbor including her neighbor's name.

<script src="https://gist.github.com/Kullsno2/f7f96d12443856cdc8f46a25d3a6f297.js"></script>

The neighbor on seeing the snippet checks whether his/her name is Akshay. If not he/she just passes the snippet to the neighbor including the neighbor's name.This goes on and on until it reaches Akshay.When Akshay reads the snippet, he matches his name to the if block and
sends back a response!

NOW HERE IS A CATCH!

Akshay cannot directly provide his response to Mythili as the teacher hasn't left the classroom still.So he returns the response to his neighbor(after all his neighbor was the one who carried the proposal message).The callback goes on and on until it reaches the original caller , Mythili. After the recursive procedure , Mythili would come to know about the response to her proposal(+/-). She would have avoided facing the failure
as she had not directly proposed to Akshay, but by through recursive calls to neighbors.

Apo postive response ah iruntha ?

```
Kalyanam than kattikittu odi polama?
Odi poyi kalyanam than kattikalama?
```
<iframe width="560" height="315" src="https://www.youtube.com/embed/fv__30kjwOc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## MTC bus ticket scenario

Here is another classic example of recursion. I have decided to include this as Morattu singles would have skipped the previous part.Suppose you board a crowded T70 via the front door.The conductor would be usually seated in his hot seat (Apdiye Jammunu irupanunga!). You have two choices , you either die a hero or live long enough to see yourself become a villain. Yeah , I mean it. You can :

1. Go without a ticket and get caught by the checking inspector in CMBT.
2. Smash everyone up and rush backward to get your ticket. You will hear countless swear words
   when you go back which when heard by your family will make them cut out their brains.

Ummm , you have a third choice. Let's #AanmeegaArasiyal , ayo sorry pa let's #Recur.

You can pass the cash with the area and the number of tickets to your neighbor. She will continue this job exactly like you did (Cash , Area , No. Of Tickets). This goes on and on until it reaches the conductor. After the cash reaches the conductor he puts the cash in his bag and returns the tickets to his neighbor. This ticket passing goes on until it reaches the original caller.

## Lollu sabha

Every single one of us would have watched lollusabha, which was one of the hit shows in VijayTV. Watch this snippet from Lollusabha's spoof on Pudhupettai movie.

<iframe width="560" height="315" src="https://www.youtube.com/embed/OaWfdesIUCU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

Let's call the guy on the middle as Ganesh and on the left as Manohar.

The video is funny and well, may be confusing in the first go.So how am I gonna relate this to recursion?

If you have carefully followed my previous examples you would have started working out!

The basic problem in the video is to provide the identity of Dhanush. Manohar(on the left), being the recursive function answers each and every question with a relationship between the first and the second person in the calling function. Read the snippet below to get a basic idea of what Manohar is doing in that video.

Ganesh asks Manohar who is this guy and Manohar keeps on telling names after names until he ends up with superstaru. After reaching superstar Ganesh changes his voice and Manohar reverses the order in which he was telling the relationships and the conversation ends when the recursion returns back to the original name , Dhanush in this case.

<script src="https://gist.github.com/Kullsno2/6a0213f5de8323e1cffd4a2bc3c672ba.js"></script>

Here is what happens in the given code.

1. Ganesh is the caller of the recursive function, yaaraivan and Manohar is the print statement in the function.
2. The main purpose of the yaaraivan function is to provide the identity of the guy with the specified name.
3. The function prints out the relationship between the guy with that name and the guy who is next to him on the list.
4. After printing out the relationship , a recursive call is made with the argument now changed to name->next, which takes the value next to the current name on the given list.
5. This goes on and on until the argument is null which is called as a result of asking
yarra superstaru?

Let's cut right here.

All this time only forward recursion has been happening with the statement :

```
yaaraivan(name->next,forward);
```

Now that all the forward recursions are finished, the backward recursion starts happening with its argument as Superstar. The relationship is now printed out in the reverse manner by the relationship function. The function knows this recursion is backward, so after printing out the relationship, it shuts it mouth and returns. The backward recursion keeps on unfolding and the relationships are printed out until Dhanush is reached, where the recursion eventually ends.

If you are confused, there is one thing you can do. Watch [this](https://www.youtube.com/watch?v=3000-SCqXrU) video
and read this part of the blog from the beginning.

## Count of Leaf Nodes in a Binary tree

This problem is one of the easiest problem involving Binary Tree and recursion.Given the root of a binary tree, you have to count the number of leaf nodes in the tree.The iterative approach to this problem would be to traverse the entire tree and check whether its a leaf node and update the counter variable.Here is the recursive approach to solve the problem:

1. If node is NULL then return 0.
2. Else If left and right child nodes are NULL return 1.
3. Else recursively calculate leaf count of the tree using below formula.

   ```
   Leaf count of a tree = Leaf count of left subtree + Leaf count of right subtree

   ```
Speak ENGLISH:

1. The root node is passed as the initial call to the function.
2. If it is null then the value 0 is returned which means that the tree is empty.
3. If the left and right child is null this means that the root is a leaf node.So the root is counted as a leaf
   and value 1 is returned.
4. If the root is not leaf then there are subtrees present on left or right or both side of the root.
5. So we recur to both the sides and get the leaf count from left and right.
6. The number of leafs in the entire tree would be obviously the number of leafs on the left and right side of the tree.
7. So we add them and return back!

Refer [this](https://www.geeksforgeeks.org/write-a-c-program-to-get-count-of-leaf-nodes-in-a-binary-tree/)
link to clarify further doubts about the topic.

## Acknowledgements

Thanks Rajkiran Rajkumar for encouraging me to do this!

Thanks for reading!
