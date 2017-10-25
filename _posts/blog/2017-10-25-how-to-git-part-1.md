---
layout: post
title: How to Git Part 1
categories: blog
tags: ['git']
excerpt: 'Everything you need to know about Git & Github.'
date: October 25, 2017
author: self

---

In this blog post I will shed light upon how to clone,add,commit,push
and pull your code to/from Github.

**Disclaimer: I am not a subject expert on git and I am
sharing my findings as I learn more about this myself.**

Prerequisites:

1. Github account.If you don't have one then create it [here](https://github.com/).
2. Git client , which we will use throughout this git process.Get it [here](https://git-scm.com/downloads).
3. A decent Internet connection with an upload speed of 2.75 Bits Per Second xD

## What is git?

A lot has been written about this, so I will not go into too much
detail about the definition. However, in one line -

> A git is a version control system for tracking changes in computer files
> and coordinating work on those files among multiple people.

## Getting Started

After getting the right tools , we are good to go on and create our 
first repository in Github.Follow the steps below:

1. Login into your github account
2. Select create new repository
3. Give a relevant and follow through the next steps.
4. Finish it!

Now you have an empty repository with a readme and a license file
of your own.

## Local Access

So you got a repository online of your own.How can you change the contents of the files
there?

Directly editing there and commiting the changes is the first thing which comes to your mind.
But you cannot always edit it online.There will be some part of the code whih requires the code 
to be stored locally.There are two ways by which you can get the repository locally.

1. Git inits and pulls.
2. Git clones.

The first method is a little bit complex.So we will stickto the second method 
whenever we need a copy our git repository locally.

## Clone

 Cloning the repository means getting an exact clone of the 
 repository in your local computer.

 1. Click clone or download option in your repository.
 2. Copy the clone url to your clipboard.
 3. Open the git bash on the location where you want the repository locally.
 4. Type the following command in your shell

```
git clone [url]
```

The git bash asks for your username and password tied to your github account.
Believe it and give the credentials.It won't do any harm.Now you got a local
copy of your repository.

## Changes

Hmm , now you have a local copy of your repository.Let's say you make changes 
to your code like adding libraries and functionalities.Your local copy will 
have additional code compared to the one which is stored on Github.How can you merge 
both the codes?

1. Add the changes to the staging area.
2. Commit the changes.
3. Push it!

## Add

The add command simply adds the changes you made to the staging area.
It prepares the code to get committed to the remote repository.The add
command is like getting a ticket to travel to a destination[remote repo].You 
just got a pass to change the code but the changes are not made in the destination
until now.Use -A to add all the files.

```
git add -A
```

You can check whether the changes are staged by typing the **git status** command.

## Commit

Commit command is like boarding the bus with the ticket issued to you.
The bus hasn't started moving yet.Commit the changes you added to
the staging area by typing the following command:

```
git commit -m "your message"
```

<figure>
	<img src="{{ site.url }}/images/how-to-git/git_commit.png" alt="commit" />
	<figcaption>Comic Courtesy : XKCD</figcaption>
</figure>

Please write a proper commit message.So that whenever you see the code at a later point
of time you will understand what the commit did.

Start the message with "Fix", "Add", "Change" instead of "Fixed", "Added", "Changed".

## Push

Now that we have boarded the bus , we have to tell the driver to start the bus
and reach the destination.We do this by ,

```
git push origin master
```

where master is the master of the branch of the current working repository.
(Branches , forks and pull requests will be dealt in a separate follow-up post).

## Final Countdown

The git bash will ask for your login credentials again and
will start pushing the code once it has been given what it 
needs.

You can bypass through this setting by globally declaring 
the username and email initially.

```
git config --global user.name "Username"
git config --global user.email mailid@example.com
```

## Acknowledgements

Ramkumar , Ganesh and Shri Shruthi 
were kind enough to teach me the basics of vcs and git.
Without them I wouldn't have had the courage to take 
up git and learn its basics.

Thanks for reading!

A follow up post ft. Branches , forks and pull requests is coming soon :)





