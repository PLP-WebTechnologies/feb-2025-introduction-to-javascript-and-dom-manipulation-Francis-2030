# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>JavaScript DOM Manipulation</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 30px;
      margin: 0;
      background-color: #f9f9f9;
      text-align: center;
    }

    header, footer {
      background-color: #333;
      color: white;
      padding: 15px;
    }

    main {
      margin-top: 30px;
    }

    button {
      padding: 10px 20px;
      margin: 10px;
      font-size: 16px;
      cursor: pointer;
      border-radius: 5px;
      border: none;
      background-color: #007bff;
      color: white;
    }

    button:hover {
      background-color: #0056b3;
    }

    .highlight {
      color: red;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <header>
    <h1>DOM Manipulation Demo</h1>
  </header>

  <main>
    <h2 id="title">Welcome to the Page</h2>
    <p id="info">Click the buttons below to interact with the page.</p>

    <button onclick="changeText()">Change Text</button>
    <button onclick="changeStyle()">Change Style</button>
    <button onclick="toggleElement()">Add/Remove Element</button>

    <div id="dynamic-area"></div>
  </main>

  <footer>
    <p>Created with 💻 by You</p>
  </footer>

  <script>
    function changeText() {
      document.getElementById('title').textContent = 'Text Changed Dynamically!';
    }

    function changeStyle() {
      document.body.style.backgroundColor = '#e0f7fa';
      document.getElementById('info').classList.toggle('highlight');
    }

    function toggleElement() {
      const area = document.getElementById('dynamic-area');
      const existing = document.getElementById('added-text');

      if (existing) {
        existing.remove();
      } else {
        const newElement = document.createElement('p');
        newElement.textContent = 'This paragraph was added with JavaScript!';
        newElement.id = 'added-text';
        area.appendChild(newElement);
      }
    }
  </script>

</body>
</html>
