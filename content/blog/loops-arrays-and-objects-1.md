---
title: Loops, Arrays and Objects Part 1
description: Working with loops, arrays and objects in Javascript
date: 2023-09-27
draft: false
tags:
  - javascript
---

Our fourth lesson in Javascript was on loops, arrays and objects. There were 6 tasks in total:

<h3> Loops </h3>
The first task was to write a loop that outputs the 7 times table to the console log. I added the functionality to take any number as a user input and return the times table of that number. Please try it yourself (see the console log for output).<br><br>

<form name="inputForm" action="" method="GET">
  Enter a number
  <br>
  <input type="text" name="inputbox" value="">
  <input type="button" name="button" value="Submit" onClick="times(this.form)">
</form>

<script>

// Print 1 to 12 times an input value to the console
function printTimes (a) {
  for (let i = 1; i <= 12; i++) {
    var x = a * i
    console.log(`${a} x ${i} = ${x}`)
  }
}

let inputValue = 1;

// Get input value and output times table
function times (form) {
    inputValue = form.inputbox.value;
  printTimes(inputValue)
}

</script>

Here is the code for my times table function.

```js

// Print 1 to 12 times an input value to the console
function printTimes (a) {
  for (let i = 1; i <= 12; i++) {
    var x = a * i
    console.log(`${a} x ${i} = ${x}`)
  }
}

let inputValue = 1;

// Get input value and output times table
function times (form) {
    inputValue = form.inputbox.value;
  printTimes(inputValue)
}
```

<h3>Arrays</h3>

The second task was to create a list of my favourite foods and print some of these to the screen. The third task was to use a for loop to print a list of these foods. Here is a link to my <a href="https://codepen.io/Katherine-York/pen/KKbRMzL">Codepen</a> for these tasks.

See <a href=""> Loops, Arrays and Objects Part 2</a> for tasks 4-6.


