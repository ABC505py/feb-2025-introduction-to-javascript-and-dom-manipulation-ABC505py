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

ANSWER:

html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>DOM Manipulation Example</title>
  <style>
    #dynamicText {
      font-size: 20px;
      color: black;
    }
    .highlight {
      color: red;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1 id="dynamicText">Welcome to My Page</h1>
  <button id="changeTextBtn">Change Text</button>
  <button id="toggleElementBtn">Add/Remove Paragraph</button>

  <div id="container"></div>

  <script src="script.js"></script>
</body>
</html>

script.js

// Change text content and style
document.getElementById("changeTextBtn").addEventListener("click", () => {
  const text = document.getElementById("dynamicText");
  text.textContent = "You've changed the heading!";
  text.classList.toggle("highlight");
});

// Add or remove an element
document.getElementById("toggleElementBtn").addEventListener("click", () => {
  const container = document.getElementById("container");
  const existingParagraph = document.getElementById("newPara");

  if (existingParagraph) {
    container.removeChild(existingParagraph);
  } else {
    const para = document.createElement("p");
    para.id = "newPara";
    para.textContent = "This paragraph was added dynamically!";
    container.appendChild(para);
  }
});


