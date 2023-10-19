---
title: Loops, Arrays and Objects Part 2 (draft)
description: Working with loops, arrays and objects in Javascript
date: 2023-09-27
draft: true
tags:
  - javascript
---

<h3>Objects</h3>

Task 4 was to create an object to hold recipe information, display the properties on screen and then use a for loop to print the recipe ingredients. Please don't try this recipe at home, it won't turn out well (I do know how to make a curry really, I promise!).

Task 5 was to create a function to print a message saying "I'm hungry, let's cook..." with the recipe title obtained from the object.

Here is my code for tasks 4 and 5. Please see the console for output.

```js
// Create recipe object

let recipe = {}

recipe.title = ["Curry"]
recipe.servings = [2]
recipe.ingredients = ["Olive oil", "Curry powder", "Onion", "Sweet potato", "Chickpeas", "Spinach"]
recipe.directions = ["Fry the onions in olive oil", "Add curry powder", "Add sweet potato"]

// Print recipe object properties to the console
console.log(recipe.title)
console.log(recipe.servings)
console.log(recipe.ingredients)
console.log(recipe.directions)

// Loop over recipe directions and print to the console
for (let i = 0; i < recipe.directions.length; i++) {
 
console.log(recipe.ingredients[i])
}

// Loop over recipe ingredients and print to the console

for (let i = 0; i < recipe.directions.length; i++) {
  console.log(recipe.directions[i])
}

// Output "I'm hungry, let's cook {recipe title}" to the console

function letsCook (recipeTitle) {
  console.log(`I'm hungry, let's cook ${recipeTitle}`)
}

letsCook(recipe.title[0])
```

<script>
    // Create recipe object

let recipe = {}

recipe.title = ["Curry"]
recipe.servings = [2]
recipe.ingredients = ["Olive oil", "Curry powder", "Onion", "Sweet potato", "Chickpeas", "Spinach"]
recipe.directions = ["Fry the onions in olive oil", "Add curry powder", "Add sweet potato"]

// Print recipe object properties to the console
console.log(recipe.title)
console.log(recipe.servings)
console.log(recipe.ingredients)
console.log(recipe.directions)

// Loop over recipe directions and print to the console
for (let i = 0; i < recipe.directions.length; i++) {
 
console.log(recipe.ingredients[i])
}

// Loop over recipe ingredients and print to the console

for (let i = 0; i < recipe.directions.length; i++) {
  console.log(recipe.directions[i])
}

// Output "I'm hungry, let's cook {recipe title}" to the console

function letsCook (recipeTitle) {
  console.log(`I'm hungry, let's cook ${recipeTitle}`)
}

letsCook(recipe.title[0])
</script>



