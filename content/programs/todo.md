<style>
body {
  font-family: sans;
  line-height: 1.5;
}

/* Limit the maximum width regardless of window size */
.container {
  max-width: 60em;
  margin-left: auto;
  margin-right: auto;
}

/* The form */
#todo {
  border: solid thin darkgray;
  padding: 1.5em;
  border-radius: 0.25em;
}

/* The unordered list containing the todos */
#todo-pane {
  padding: 0;
}

/* The todos themselves */
#todo-pane li {
  display: flex;
  max-width: 20em;
  align-items: center;
  background-color: lightyellow;
  border: thin orange solid;
  border-radius: 0.25em;
  padding: 0.5em;
  margin: 1em 0;
}

/* A todo that was just created */
.just-created {
  box-shadow: 0 0 20px 1px orange;
}

/* The image of a flag within a todo */
#todo-pane li img {
  width: 1em;
  padding-right: 1rem;
}

/* The small text in the footer */
small {
  font-size: small;
  font-style: italic;
}
</style>

<h3>To Do List</h3>

<div class="container">

<form id="todo">
    <label for="title">Title</label>
    <input type="text" name="title" id="title" required>
    <label for="priority">Priority</label>
    <select name="priority" id="priority">
      <option value="low">Low</option>
      <option value="medium" selected>Medium</option>
      <option value="high">High</option>
    </select>
    <button>Add</button>
  </form>

  <!-- This is an empty container for use by javascript. -->
  <ul id="todo-pane"></ul>
  
  <footer>
    <small>
      Flag images used with thanks from <a href="https://www.iconfinder.com/iconsets/prettyoffice8">https://www.iconfinder.com/iconsets/prettyoffice8</a>.
    </small>
  </footer>
</div>

<script>
// Store the URL of an image for each priority level.
const priorityImages = {
  low: 'https://cdn1.iconfinder.com/data/icons/prettyoffice8/256/Flag-green.png',
  medium: 'https://cdn1.iconfinder.com/data/icons/prettyoffice8/256/Flag-yellow.png',
  high: 'https://cdn1.iconfinder.com/data/icons/prettyoffice8/256/Flag-red.png',
};

// Get the form by ID from the forms collection.
const form = document.getElementById("todo");
// Get the todo pane (the 'ul' element) to insert todos into.
const todoPane = document.querySelector("ul");
// Get the text input for the title. We'll read from this when creating the todo.
const titleInput = document.getElementById("title");
// Get the priority select element. We'll read from this when creating the todo.
const prioritySelect = document.getElementById("priority");
// Get a *live* list of all elements with the 'todo' class.
const allTodos = document.querySelectorAll(".todo");
// const all Todos = getElementsByClass("todo")

form.addEventListener('submit', createTodo)

function getPriorityImage (level) {
  switch (level) {
    case "low":
      return(priorityImages.low)
    case "medium":
      return(priorityImages.medium)
    case "high":
      return(priorityImages.high)
  }
}

function createTodo(event) {
  const priorityLevel = prioritySelect.value;
  const title = titleInput.value;
  // Create the text node with the variable 'title'.
  const text = document.createTextNode(title);
  const img = document.createElement('img');
  img.src = getPriorityImage(priorityLevel);
  img.style.marginLeft = '5px';
  // Create a new list item element to contain the text node and image.
  const listItem = document.createElement('li');
  // Add the text node to the list item element.
  listItem.appendChild(text);
  listItem.appendChild(img);
  // Add the list item to the list
  todoPane.appendChild(listItem);
  // Prevent the form being submitted to the server
  event.preventDefault() ;
  // Reset form to clear title input
  form.reset();
  // Remove class from previous list item
  const previousListItem = document.querySelector(".just-created")
  if (previousListItem) {
    previousListItem.classList.remove("just-created")
  }
  // Add class to new list item
  listItem.classList.add("just-created");
  // Console log list item with class "just-created"
  justCreated = document.querySelector(".just-created")
  console.log(justCreated)
  // Add a click handler that deletes list item on click
  justCreated.addEventListener('click', deleteItem)
}

function deleteItem (event) {
  element = event.currentTarget;
  element.remove();
}
</script>