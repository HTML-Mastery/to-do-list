# to-do-list
Basic To Do App

## HTML

```html
<div class="todo-container">
        <h1>To-Do List</h1>
        <input type="text" id="taskInput" placeholder="New Task">
        <ul id="taskList">
            <!-- Tasks will be added dynamically here -->
        </ul>
        <button onclick="addTask()">Add Task</button>
    </div>
```

## CSS

```css
      body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .todo-container {
            width: 300px;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            box-sizing: border-box;
        }

        h1 {
            text-align: center;
            color: #333;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #eee;
            padding: 8px 0;
        }

        input[type="checkbox"] {
            margin-right: 8px;
        }

        input[type="text"] {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
            margin-bottom: 10px;
        }

        button {
            background-color: #4caf50;
            color: #fff;
            border: none;
            padding: 8px 12px;
            border-radius: 4px;
            cursor: pointer;
        }
```

## JavaScript

```js
function addTask() {
            const input = document.getElementById("taskInput");
            const ul = document.getElementById("taskList");
            const li = document.createElement("li");
            const checkbox = document.createElement("input");
            checkbox.type = "checkbox";
            li.appendChild(checkbox);
            li.appendChild(document.createTextNode(input.value));
            ul.appendChild(li);
            input.value = "";
        }
```
