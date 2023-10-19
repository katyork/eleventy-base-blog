---
title: Loops, Arrays and Objects Part 3 (draft)
description: Working with loops, arrays and objects in Javascript
date: 2023-09-27
draft: true
tags:
  - javascript
---

<h1>Favourite Jazz Musicians / Bands</h1>

For this task I wrote two functions - the first prints a list of favourite artists (an array) to the console using a for loop. The second takes an artist name as user input and adds it to the array.

<form name="artistForm" action="" method="GET">
  Add name of artist to the list
  <br>
  <input type="text" name="inputbox" value="">
  <input type="button" name="button" value="Submit" onClick="addArtist(this.form)">
</form>

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