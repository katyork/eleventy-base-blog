---
title: Loops, Arrays and Objects Part 3 (draft)
description: Working with loops, arrays and objects in Javascript
date: 2023-09-27
draft: true
tags:
  - javascript
---

The takeaway task from our first session on loops, arrays and objects was to create an array and then to create two functions - the first iterates over the array and prints each item to the console, the second adds another item to the list and prints the updated list to the console.

<h3>Favourite Jazz Musicians / Bands</h3>

<form name="artistForm" action="" method="GET">
  Add name of artist to the list
  <br>
  <input type="text" name="inputbox" value="">
  <input type="button" name="button" value="Submit" onClick="addArtist(this.form)">
</form><br>

Here is my code. See the console for output.

```js
artists = ["Ben Webster", "Eddie Harris", "John Coltrane", "Sons of Kemet", "Ezra Collective", "Gogo Penguin"]

// Print list items to console
function logList (list) {
  for (let i = 0; i < list.length; i++) {
    console.log(list[i])
  }
}

logList(artists)

// Add artist to list and print updated artist list to console
function addArtist (form) {
    var inputValue = form.inputbox.value;
  artists.push(inputValue)
  logList(artists)
}
```

<script>
artists = ["Ben Webster", "Eddie Harris", "John Coltrane", "Sons of Kemet", "Ezra Collective", "Gogo Penguin"]

// Print list items to console
function logList (list) {
  for (let i = 0; i < list.length; i++) {
    console.log(list[i])
  }
}

logList(artists)

// Add artist to list and print updated artist list to console
function addArtist (form) {
    var inputValue = form.inputbox.value;
  artists.push(inputValue)
  logList(artists)
}

</script>