# Ex03 To-Do List using JavaScript

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM

## Index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple To-Do App</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h1>My To-Do List</h1>
    <div class="input-box">
      <input type="text" id="taskInput" placeholder="Add a new task">
      <button id="addBtn">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>

  <script src="script.js"></script>
</body>
</html>


```
## Style.css
```
body {
  font-family: Arial, sans-serif;
  background: #f0f8ff;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.container {
  background: white;
  padding: 20px 30px;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  width: 300px;
  text-align: center;
}

h1 {
  color: #333;
}

.input-box {
  display: flex;
  margin-top: 15px;
}

input {
  flex: 1;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 8px;
}

button {
  margin-left: 8px;
  padding: 8px 12px;
  border: none;
  background: #4caf50;
  color: white;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background: #45a049;
}

ul {
  list-style: none;
  padding: 0;
  margin-top: 20px;
}

li {
  background: #e7f3fe;
  margin-bottom: 8px;
  padding: 10px;
  border-radius: 8px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li.completed {
  text-decoration: line-through;
  color: gray;
}

.delete-btn {
  background: red;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 3px 8px;
  cursor: pointer;
}

```

## Script.js
```
const input = document.getElementById("taskInput");
const addBtn = document.getElementById("addBtn");
const taskList = document.getElementById("taskList");

addBtn.addEventListener("click", addTask);

function addTask() {
  const taskText = input.value.trim();
  if (taskText === "") return alert("Please enter a task!");

  const li = document.createElement("li");
  li.textContent = taskText;

  li.addEventListener("click", () => {
    li.classList.toggle("completed");
  });

  const delBtn = document.createElement("button");
  delBtn.textContent = "X";
  delBtn.className = "delete-btn";
  delBtn.onclick = () => li.remove();

  li.appendChild(delBtn);
  taskList.appendChild(li);
  input.value = "";
}

```

## OUTPUT

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ea3a91dc-e329-4efe-a66b-f4f7525d2593" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
