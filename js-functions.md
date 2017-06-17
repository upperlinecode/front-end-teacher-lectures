# Javascript Functions

## SWBAT
+ Explain that the purpose of using functions is to make code less error-prone, more readable, and more DRY (less repetition.)
+ Use the proper syntax of a javascript functions
+ Create functions with multiple arguments.


## Hook
Put up the following "black boxes" and have the students give them names and explanations (eg. box 1 doubles the input, we will call it `doubleInput`)

1.
```
3 ——> 6
4 ——> 8
25 —> 50
```

2)
```
CAT —> DBU
HELLO —> IFMMP
SOLAR —> TPMBS
```
3)
```
Nicki, 10 -> Nicki was born in 2007
Joe, 21 -> Joe was born in 1996
Andrea, 45 —> Andrea was born in 1972
```
4)

```
3.9 -> A
3.0 -> B
1.0 -> F
```

What we've done here is think about the black boxes as machines that do something when they are given data. That is exactly what functions do in javascript, they accept information, do something to it, and then return new output. Instead of having to write a bunch of code over and over, we can just call a function by the name we've given it.

## Lecture
Let's look a the structure of a function:

```js
function functionName(parameter){
  //Code in here
  x = parameter + 1
  return x
}
```

In the function above, you'll notice that there are 4 main parts to a function definition (NICO):
+ **Name** - What is the function named so we can call it later?
+ **Inputs** - What are the inputs (which we call parameters)? Sometimes a function does not have any inputs, but it usually does)
+ **Code** - What code gets run when the function is called?
+ **Output** - What data gets output in the `return` statement?

Let's do an example by building the `double` function:

```js
function double(num){
  var newNum = num*2;
  return newNum;
}
```
We've defined the function, but we need to CALL it in order to use it.

```js
double(2) // Returns 4
double(6) // returns 12
double(1000) //returns 2000
```
Sometimes we need multiple pieces of data to come in to our function:

```js
function addTwoNumbers(a,b){
  return a+b
}
```


**Mini Challenge: Tip Calculator**
Create a function called `tipCalculate` that takes in the total bill and the tip percentage as inputs, and returns the amount that you need to tip your waiter.

(Have students try to do this individually for 5 minutes and then walk them through it as a class)

```js
tipCalculate("$20", "15%") // returns $3
tipCalculate("$100", "20%") // returns $20
```
(Notice that we are starting with strings, so need to get rid of symbols and convert to float before we can calculate the tip)

Answer:
```js
function tipCalculate(cost, percentTip){
  var numberCost = parseFloat(cost.replace("$", ""))
  var tipPercentage = parseFloat(percentTip.replace("%", ""))
  var finalTip = numberCost * tipPercentage / 100
  return finalTip
}
```

### Twitter Functions Mini lab

+ Create a function `twitterLength` that takes in a string and tells you if it is too long for twitter or not.

+ Create a function `addHashtag` that takes in a string and adds the string `#javascriptrules` to the end of it.

+ Create a function called `textToTweet` that changes "for" to "4", "you" to "u", and "great" to "gr8".
