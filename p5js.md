# Javascript with P5js - Teacher Lecture Notes

SWBAT:
* Use the P5 library to build interactive art pieces.
* Integrate variables, conditionals, functions, and event listeners into p5 projects.
* Place and manipulate shapes, images, and text on the canvas
* Use the p5 documentation
* Use built in p5 functions (eg. random(), mouseClick(), etc) to made pieces dynamic.


## Hook

**Prep: Look up a number of cool p5 projects. A good starting point is p5js.org**

We talk alot about using code to build applications and to create functional websites, often for social good or for businesses. But today, we're going to change course for a bit. Today we're going to *make art*. Yes, code can be artistic - take a look at these amazing projects.

**Show projects**

To build all of these, the artists used the tools that you have (HTML and CSS), and added in a new language and library: Javascript and P5. Javascript is the languages that makes all pages on the web interactive and dynamic. P5 is a library (a collection of code written by other developers) that allows us to really easily create shapes on a canvas, and then manipulate those shapes using built in functions. By then end of today's class you all are going to be building your own art projects, and if you really enjoy this part of the class, you can pick p5 to work with for your final project.

## Key Points and Sequence for code along

### Setup

+ Start by showing the students that a p5 projects is just an html page linking to the p5 library and to an empty javascript file. Have them all build this themselves the first time (but then offer them the boilerplate that they can clone and download)

**Ensure all students are set up**

+ Create a canvas in the setup() function using `canvas(600,800)`. Question the students to see if they can figure out what those two arguments are (width and height). Explain that the setup function only gets called one time at the loading of the page. Anything we want to happen only once at the start should be in here. Set the background color to green using `backgound(0,255,0)`. This sets the bg color once at the start.

+ Explain that the 3 numbers stand for red, green and blue, or RGB.
**Give students 2 minutes to choose a new color for their backgrounds**

+ Bring up the analogy of an animated flipbook (like the early movies). We flip through really fast and it looks like things are moving. This is the same in p5: the `draw()` function draws each frame or page at a rate of 60 times a second. Anything we put in here will get re-rendered over and over. If we place things in a static position, it doesn't make a difference, but if we place with variables it does.

### Shapes, color and the coordinate system

+ Place a circle and a square on the canvas in the draw function but do not open the browser to visualize it:

```js
function draw() {
  fill(255,0,0);
  rect(30,60,200,100);
  fill(255,0,0);
  ellipse(400,500,50,80);
}
```
**Ask the students what they think the screen will look like when we run this (1 minutes). Run the code and then ask the students if their predictions were correct. If not, what do we know now about the functions we used (fill, rect, ellipse), their arguments, the coordinate system**

+ Explain that the coordinate system starts at the top left and increases down and to the right.

+ Explain the syntax of the fill, rect, and ellipse functions.

+ Show the students the [p5js reference pages](www.p5js.org/reference) and encourage them to figure out stroke, fill, strokeWidth, other shapes, etc.

**Give the students 10-15 minutes to tinker and build. Mini challenges include the Olympic rings and the logo design challenges**

### Variables

+ Sometimes we want to store information, say a number or a string of characters so that we can use it in a bunch of places (if this is an advanced class, just remind students of variables).

+ Show students a painful example of placing many shapes of the same size, or of incrementing size. Show them that by replacing the width and height arguments with a variable that our code gets neater, easier to update, and easier to debug.

```js
//ORIGINAL PAINFUL
function draw() {
  fill(255,200,0);
  ellipse(100,300,50,50);
  ellipse(200,300,60,60);
  ellipse(300,300,70,70);
  ellipse(400,300,80,80);
  ellipse(500,300,90,90);
}

//VARIABLES BETTER!
var xPosition = 100; // Notice the variable declaration outside
var yPosition = 300; // Why? So we can use the variables inside of other functions.
var diameter = 50;

function draw() {
  fill(255,200,0);
  ellipse(xPosition,yPosition,diameter,diameter);
  ellipse(xPosition+100,yPosition,diameter + 10,diameter + 10);
  ellipse(xPosition+200,yPosition,diameter + 20,diameter + 20);
  ellipse(xPosition+300,yPosition,diameter + 30,diameter + 30);
  ellipse(xPosition+400,yPosition,diameter + 40,diameter + 40);
}
```

+ We can also use *built in variables* that we don't have to define:
  + `width` and `height` for the width and height of the canvas.
  + `mouseX` and `mouseY` for the x and y coordinates of the mouse.

```js
function draw() {
  fill(255,200,0);
  ellipse(mouseX, mouseY, width/10, height/5)
}
```
**Ask for student predictions. Where will the ellipse be? Will it move? What will happen to it's size if we change the size of the canvas?**

The circle follows the mouse because it's x and y positions are the mouseX and mouseY variables. It will change in size relative to the canvas because it's width and height use `width` and `height` as variables.

**Mini Challenges: Look at the variables mini challenges in the student labs section**
