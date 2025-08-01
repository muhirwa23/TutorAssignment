# TutorAssignment
##  **Assignment Title: Interactive Student Registration Web App**

### 📌 **Work Description**

You are required to build a simple and interactive **Student Registration Web Application** using **HTML**, **CSS**, and **JavaScript**.

The user (student) will enter their personal information through a form, and upon submission, the app will:

* Validate and process the inputs using JavaScript.
* Display a summary of the entered information.
* Show custom messages based on the user's age and favorite subject.
* Include a toggle button to switch between **Light Mode** and **Dark Mode**.

This project will help you apply the key JavaScript concepts you have learned so far, such as:

* Variables
* DOM manipulation
* Conditional statements (`if`, `else`, `switch`)
* Loops (`while`)
* Event handling

###  **Learning Objectives**

By completing this project, you will:

* Understand how to handle form inputs and interact with the DOM.
* Practice writing JavaScript logic to make real-time decisions.
* Learn how to style and manipulate the page using CSS and JavaScript together.
* Enhance your problem-solving and debugging skills.

### 📋 **Project Instructions**

You are given:

* `index.html` → already designed form and structure.
* `style.css` → already styled for layout and theme.
* `script.js` → empty JavaScript file with step-by-step comments as guidance.

Your task is to:

1. Complete the JavaScript code based on the provided comments.
2. Make the web app interactive and responsive to the user input.
3. Ensure the app behaves correctly according to all instructions in the comments.

###  **Expected Features**

*  User fills in: name, age, gender, subject.
*  JavaScript displays results dynamically below the form.
*  Age-based message appears:

  * Under 18: "You are a high school student."
  * 18 or above: "You might be in university."
*  Subject-based message appears using `switch`:

  * Math → “You’re a numbers lover.”
  * English → “Words are your power.”
  * Science → “Future innovator!”
* Light/Dark mode toggle button that changes the theme.
*  Uses `while` loop to ensure name is not empty.

### 📁 **Deliverables**

Submit your final project with the following files:

* `index.html`
* `style.css`
* `script.js` (your completed JavaScript work)

You may submit:

* As a .zip folder
* As a GitHub repository
* Or hosted on platforms like CodeSandbox, GitHub Pages, etc.


## 📁 Folder Structure

```
/student-registration
├── index.html
├── style.css
└── script.js   ← (they will fill this)
```



###  `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Student Registration</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="container">
    <h1>Student Registration Form</h1>
    
    <form id="studentForm">
      <label for="name">Full Name:</label>
      <input type="text" id="name" placeholder="Enter your name" />

      <label for="age">Age:</label>
      <input type="number" id="age" placeholder="Enter your age" />

      <label for="gender">Gender:</label>
      <select id="gender">
        <option value="">Select gender</option>
        <option value="Male">Male</option>
        <option value="Female">Female</option>
      </select>

      <label for="subject">Favorite Subject:</label>
      <select id="subject">
        <option value="">Select subject</option>
        <option value="Math">Math</option>
        <option value="English">English</option>
        <option value="Science">Science</option>
      </select>

      <button type="submit">Register</button>
    </form>

    <button id="toggleTheme">Toggle Light/Dark Mode</button>

    <div id="resultArea">
      <!-- Student info will appear here after JS DOM manipulation -->
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
```

---

###  `style.css`

```css
body {
  font-family: Arial, sans-serif;
  background-color: #f0f0f0;
  color: #333;
  margin: 0;
  padding: 0;
}

.container {
  width: 90%;
  max-width: 600px;
  margin: 30px auto;
  background: white;
  padding: 25px;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

input, select, button {
  padding: 10px;
  font-size: 16px;
}

button {
  background-color: #007BFF;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}

#resultArea {
  margin-top: 30px;
  padding: 15px;
  background-color: #eaf6ff;
  border-radius: 5px;
}

/* Dark mode class */
.dark-mode {
  background-color: #1e1e1e;
  color: #f1f1f1;
}

.dark-mode .container {
  background-color: #2c2c2c;
}

.dark-mode input, .dark-mode select, .dark-mode button {
  background-color: #444;
  color: #fff;
  border: 1px solid #555;
}
```

---

###  `script.js` (You are going  to do that)

```js
// 1. Select the form and resultArea using document.getElementById

// 2. Add an event listener to the form's "submit" event
//    - Use preventDefault() to stop form from reloading the page

// 3. Inside the submit handler:
//    a. Get values of name, age, gender, and subject using .value
//    b. Use a WHILE loop to keep asking (prompt) if name is empty
//    c. Use IF/ELSE to check age:
//       - If under 18 → "You are a high school student."
//       - Else → "You might be in university."
//    d. Use SWITCH on subject to set a comment:
//       - Math → “You’re a numbers lover.”
///      - English → “Words are your power.”
//       - Science → “Future innovator!”
//    e. Create a paragraph or div and insert all data + messages into resultArea using innerHTML or createElement + appendChild

// 4. Toggle theme:
//    - Select the toggleTheme button
//    - On click, add/remove class 'dark-mode' to the body

// Hint: Use template literals (`Hello ${name}`) to build your message
```

