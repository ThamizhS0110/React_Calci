# Ex04 Simple Calculator - React Project
## Date:19.03.2026

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
#### app.jsx
```
import React, { useState } from "react";

const Calculator = () => {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const calculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div style={styles.container}>
      <h2>Calculator</h2>

      <input
        type="text"
        value={input}
        readOnly
        style={styles.input}
      />

      <div style={styles.grid}>
        <button onClick={clearInput}>C</button>
        <button onClick={() => handleClick("/")}>/</button>
        <button onClick={() => handleClick("*")}>*</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>

        <button onClick={() => handleClick("0")}>0</button>
        <button onClick={() => handleClick(".")}>.</button>

        <button onClick={calculate} style={styles.equal}>
          =
        </button>
      </div>
    </div>
  );
};

const styles = {
  container: {
    width: "250px",
    margin: "50px auto",
    padding: "20px",
    borderRadius: "10px",
    background: "#2d2d44",
    color: "white",
    textAlign: "center",
  },
  input: {
    width: "100%",
    height: "40px",
    marginBottom: "10px",
    fontSize: "18px",
    textAlign: "right",
    padding: "5px",
  },
  grid: {
    display: "grid",
    gridTemplateColumns: "repeat(4, 1fr)",
    gap: "10px",
  },
  equal: {
    gridColumn: "span 2",
    backgroundColor: "#ff5757",
    color: "white",
  },
};

export default Calculator;
```


## OUTPUT
<img width="1916" height="1197" alt="image" src="https://github.com/user-attachments/assets/a59638e0-19bb-4a93-ac50-dcf966e8a736" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
