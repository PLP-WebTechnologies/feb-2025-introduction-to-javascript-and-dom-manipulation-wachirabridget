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
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript DOM Manipulation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        button {
            padding: 10px;
            margin: 10px;
            cursor: pointer;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 5px;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to JavaScript DOM Manipulation</h1>
    </header>
    <main>
        <p id="text">Click the button to change this text!</p>
        <button id="changeTextBtn">Change Text</button>
        <button id="toggleElementBtn">Add Element</button>
        <div id="elementContainer"></div>
    </main>
    <script>
        document.addEventListener("DOMContentLoaded", function () {
            const textElement = document.getElementById("text");
            const changeTextBtn = document.getElementById("changeTextBtn");
            const toggleElementBtn = document.getElementById("toggleElementBtn");
            const container = document.getElementById("elementContainer");
            changeTextBtn.addEventListener("click", function () {
                textElement.textContent = "Text has been changed!";
                textElement.style.color = "blue";
                textElement.style.fontWeight = "bold";
            });
            toggleElementBtn.addEventListener("click", function () {
                if (container.innerHTML === "") {
                    const newElement = document.createElement("p");
                    newElement.textContent = "A new paragraph has been added!";
                    newElement.style.color = "green";
                    container.appendChild(newElement);
                    toggleElementBtn.textContent = "Remove Element";
                } else {
                    container.innerHTML = "";
                    toggleElementBtn.textContent = "Add Element";
                }
            });
        });
    </script>
</body>
</html>

