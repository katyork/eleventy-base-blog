---
title: Functions and Control Flow Practical
description:
date: 2023-09-26
draft: true
tags:
  - javascript
---

This week's practical session consisted of 3 tasks. 

<h3>Percentage Calculator</h3>
The first task was to create a percentage calculator. Here is a link to my <a href="https://codepen.io/Katherine-York/pen/PoXdNPr">Codepen</a> for this task.

<h3>Switch Statement</h3>
We used a switch statement to output different messages depending on the drink selected. See the console for output.

<form name="inputForm" action="" method="GET">
  <h5>Drinks Order</h5>
  Please choose your drink size.
  <br>
    <input type="radio" id="small" name="size" value="small">
    <label for="small">Small</label><br>
    <input type="radio" id="medium" name="size" value="medium">
    <label for="medium">Medium</label><br>
    <input type="radio" id="large" name="size" value="large">
    <label for="large">Large</label><br>
  <br>
  Please choose your drink.
  <br>
    <input type="radio" id="lemon" name="drink" value="lemon">
    <label for="lemon">Lemonade</label><br>
    <input type="radio" id="orange" name="drink" value="orange">
    <label for="orange">Orangeade</label><br>
    <input type="radio" id="cola" name="drink" value="cola">
    <label for="cola">Cola</label><br>
  <br>
  <input type="button" name="button" value="Place Order" onClick="placeOrder(this.form)">
  <br>
</form>

<script>
  function drinkOrder (size, drink) {
  switch (drink) {
    case 'lemon':
      return `You have ordered a ${size} lemonade`;
    case 'orange':
      return `You have ordered a ${size} orangeade`;
    case 'cola':
      return `You have ordered a ${size} cola`;
  }
}

function placeOrder (form) {
  let inputSize;
  let inputDrink;
  inputSize = form.size.value;
  inputDrink = form.drink.value;
  
  alert(drinkOrder(inputSize, inputDrink));
}
</script>

Here is my code:
```js
function drinkOrder (size, drink) {
  switch (drink) {
    case 'lemon':
      return `You have ordered a ${size} lemonade`;
    case 'orange':
      return `You have ordered a ${size} orangeade`;
    case 'cola':
      return `You have ordered a ${size} cola`;
  }
}

function placeOrder (form) {
  let inputSize;
  let inputDrink;
  inputSize = form.size.value;
  inputDrink = form.drink.value;
  
  alert(drinkOrder(inputSize, inputDrink));
}
```

<h3>Calculator</h3>

We created a calculator taking inputs of two numbers and an operator and returning the answer. I added validation to check the number inputs were numbers and the operator was a valid operator. 

Here is a link to my <a href="https://codepen.io/Katherine-York/pen/LYMOePP">Codepen</a> for this task.