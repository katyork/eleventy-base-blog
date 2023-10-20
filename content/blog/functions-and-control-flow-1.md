---
title: Functions and Control Flow Part 1
date: 2023-09-25
draft: false
tags:
    - javascript
---

I wrote my first Javascript functions!

<h3>Concanating Strings / Template Literals</h3>

The first task was to concatenate two strings (a first name and a last name) and output "My name is..." to the console log. I used template literals to construct the sentence.

Here is my code. See the console for output!

```js
function sentence (name) {
    output.innerHTML = (`My name is ${name}`)
}

function getName(firstName, lastName) {
    return(`${firstName} ${lastName}`);
}

name = getName("Katherine", "York")

sentence(name)
```
<script>

function sentence (name) {
    console.log(`My name is ${name}`)
}

function getName(firstName, lastName) {
    return(`${firstName} ${lastName}`);
}

name = getName("Katherine", "York")

sentence(name)

</script>

<h3> If/Else Statements </h3>
I also wrote a function to tell you the appropriate clothes to wear based on the temperature outside using if else statements.

<h4>Clothes Check</h4>
<form name="tempForm" action="" method="GET">
  What is the temperature in degrees F?
  <br>
  <input type="text" name="inputbox" value="">
  <input type="submit" name="button" value="Submit" onClick="getTemp(this.form)">
</form>

<p id="output"></p>

<script>
const output = document.getElementById("output")

clothesCheck = (temp) => {
  if (temp < 0) {
    return("Stay inside");
  } else if (temp < 30) {
    return("Wear a coat and hat");
  } else if (temp < 50 ) {
    return("Wear a coat");
  } else {
    return("Just pants and vest is fine");
  }
}

function getTemp (form) {
    var inputValue = form.inputbox.value;
 alert(clothesCheck(inputValue))
 output.innerHTML = clothesCheck(inputValue)
}
</script>

Here is my code:

```js
clothesCheck = (temp) => {
  if (temp < 0) {
    return("Stay inside");
  } else if (temp < 30) {
    return("Wear a coat and hat");
  } else if (temp < 50 ) {
    return("Wear a coat");
  } else {
    return("Just pants and vest is fine");
  }
}

function getTemp (form) {
    var inputValue = form.inputbox.value;
 alert(clothesCheck(inputValue))
}
```
