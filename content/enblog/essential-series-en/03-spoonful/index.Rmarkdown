---
title: "How to set (and find) the working directory (#01)"
weight: 3
subtitle: "How to ask RStudio to import our data"
excerpt: "How to ask RStudio to import our data"
date: 2022-10-19
draft: false
---

It is possible to create data in RStudio's **scripts**. However, we'd usually want to import our own data sets and work with them, right? For example, we may import some data files from a psycholinguistic study, make some transformations and use them for statistical tests. In order to do that, we should always tell RStudio (*very politely, of course*) **where** it may find our files. With this in mind, today we'll learn more about ```setwd()``` and ```getwd()``` functions. 

## What's the working directory? 

The **working directory** is, basically, the computer folder in which you've stored your data files. Hence, if we want RStudio to find those data files, you should first tell it what is the right **path** to this folder.

## setwd()

We have a lot of different files in our computers, each in a folder, right? Essentially, each of these files can be found with a **path**. In other words, each individual file/folder has an unique **path** to be found.

> For example, let's assume that you have the "documents" folder and a folder called "Masters" inside of it and a subfolder called "Research_Data" inside the later, such as this:

![](images/paste-47F99758.png)

> It is possible to see that the folder "Research_Data" is inside "Masters", which, in turn, is inside "Documents", which is, in turn, inside "Este Computador" ("*this computer*", in Portuguese). Well, this is **exactly** what you're supposed to tell RStudio, since, unfortunately, it is (still) not able to find by itself in what folder you've stored your files. <br>
There are plenty of ways to [find][1] the files' path on Windows (I've never used Mac, so, unfortunately, I don't know how it should be done in a Macbook).

That being said, you literally just need to tell RStudio with ```setwd()``` (which stands for *set working directory*) which is the correct path to the folder in which you've stored your data files:

> setwd("C:/Users/laris/Documents/Masters/Research_Data")

Another way of doing the exact same thing is by using RStudio's **menu**, which, by default, is on the console's right side:

![](images/paste-24016D46.png)

As I've just mentioned above, there are different ways of finding the path to your desired folder in Windows, but what if you'd like to find it inside RStudio?

## getwd()

This is where ```getwd()``` comes in hand. We may use ```getwd()``` (which stands for *get working directory*) in order to make RStudio tell us which is our current working directory:

> getwd()
>
> \[1\] "C:/Users/laris/Documents/Masters/Research_Data"

You should **always** check if your data files are in the correct folder. In addition to that, you should **always** check if you're, indeed, working in the right working directory. It is pretty common to get error messages such as "it wasn't possible to find file X" or "file X does not exist in the current working directory", these messages appear because you're working in the wrong working directory!

In order to save some time typing the whole thing, you may use ```getwd()``` output and copy it in ```setwd()``` . &#128521;

Finally but not least, nowadays it is recommended to use *projects* rather than *setwd()*, but let's cross that bridge when we come to it, all right? We'll talk about it too. See you there!

&#128021; Au-au! Today we saw that each file in our computers has a *path* and that we should always tell RStudio the correct path to the folder in which our data files are stored. We may do that using ```setwd()```. This folder will become our *working directory*. We may use RStudio to tell us which is the current working directory using ```getwd()```. It is also possible to use the later output in ```setwd()``` in order to save some typing time. See you soon!


[1]:https://www.wikihow.com/Find-a-File%27s-Path-on-Windows
