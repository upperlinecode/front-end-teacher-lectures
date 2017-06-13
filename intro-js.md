# Javascript Basics

## SWBAT:

+ Use the console to test and debug javascript
+ Connect a javascript file to an html file
+ Use `alert()`, `prompt()` and `console.log()` functions
+ Understand and use variables to store data.
+ Use built in methods to manipulate data (.toUpper, etc)
+ Use a for loop to iterate over an array
+ Use vanilla javascript to show how the dom can be manipulated (as a precursor to jquery)


## Lecture Overview:

We've looked at p5 as a fun way to get introduced to Javascript - today we're going to dive deep into the language itself and learn how it interacts with HTML pages to make them dynamic. Today's lesson is THE FOUNDATION to everything else we do in this class. Javascript is the core language that is used to make every website interactive. Javascript moves us from STATIC to DYNAMIC.

Let's take a look at some websites that are amazing at using Javascript. See if you can figure out the things that require JS to work:

+ [Wrapgenius](http://www.wrapgenius.me/)
+ [Histography](http://www.histography.io/)
+ [The Boat](http://www.sbs.com.au/theboat/)

**Pair-Share: Ask the students where they see javascript in play - what are the dynamic aspects of each site?**

Everyone here has done some computer science, so we're going to go through the syntax and fundamentals of JS pretty fast and get to DOM manipulation as quickly as we can.

## Console

Let's start with the console. The console is the place in the browser where you can TEST your code - (this is sort of like irb for the students who have studied ruby). We can open it up in Chrome by typing `command` + `shift` + `j` on a mac, or `ctrl` + `shift` + `j` on a PC.


**Have students open the console and try some basic commands, adding numbers, concatenating text, etc**

```js
var age = 10
oldage = age + 15

sentence = "I am " + oldage + " years old"
sentence
```

## Separate JS file

We can also run javascript from a separate file with a `.js` extension.

**Walk the students through creating a new HTML and JS file and linking the two using the `<script>` tag in the HTML head section**

```HTML
<!DOCTYPE html>
<html>
  <head>
    <script type="text/javascript" src="myscript.js"></script>
  </head>
  <body>

  </body>
</html>
```

## Prompt, Console.log, alert

There are some very quick functions that we are going to play with, even though later on you won't want to use the prompt and alert too much.

+ `alert()` creates a popup that the user has to accept (ugh!)
+ `prompt()` creates a popup with a text bar for the user to fill out. If we sent the prompt equal to a variable then we can use the user input.
+ `console.log()` let us print data to the console. This is super useful for debugging (and is like print or puts in ruby/python)

**Mini-Break: Have students create popups and prompts**

## Data Types

+ Integers
+ Floats
+ Strings
+ Arrays
+ Objects

## Conditionals

## Functions

## Iterating/Looping
