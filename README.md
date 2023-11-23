# Debuggings Assessments for Js for Hyper Island School

## Description of the bugs:

- **Line 3**  
  **_Syntax error_**: different type of quotation marks  
  Found error in console pointing to incorrect line

  `"search’` => `"search”`

- **Line 3**  
  **_Syntax error_**: Missing (#) to select ID Tag  
  Found error in console pointing to incorrect line

  `"search”` => `"#search”`

  > "Uncaught TypeError: Cannot read properties of null (reading 'addEventListener')"

- **Line 4**  
  **_Syntax error_**: Missing (#) to select ID Tag  
  Found error in console pointing to incorrect line

  `"city”` => `"#city”`

  > "Uncaught TypeError: Cannot read properties of null (reading 'addEventListener')"

- **Line 5**  
  **_Syntax error_**: Missing (#) to select ID Tag  
  Found error in console pointing to incorrect line

  `"temp”` => `"#temp”`

  > "Uncaught TypeError: Cannot read properties of null (reading 'addEventListener')"

- **Line 6**  
  **_Syntax error_**: Missing (#) to select ID Tag  
  Found error in console pointing to incorrect line

  `"message”` => `"#message”`

  > "Uncaught TypeError: Cannot read properties of null (reading 'addEventListener')"

- **Line 4**  
  **_Syntax error_**: typo missing "o"  
  Found error in console pointing to incorrect line

  `querySelectr` => `querySelector`

- **Line 40**  
  **_Syntax error_**: Missing parenthesis for (e) parameter  
  Found error in console pointing to incorrect line

  `e` => `(e)`

- **Line 41**  
  **_Runtime error_**: Missing `e` object attached to the built-in function  
  Because the page making the default behaviour after clicking

  `preventDefault();` => `e.preventDefault();`

- **Line 19**  
  **_Syntax error_**: We should use Backticks instead of Double quote because we have variable inside.  
  Found the error in the Dom when you click search show `${temp}°C`

  `“${temp}°C”` => `${temp}°C`

- **Line 17**  
  **_Runtime error_**: missing a key in the middle `main`.  
  Found it in the display where I got the result `NaN` . I checked the JSON file.

  `let temp = data.temp - 273.15;` => `let temp = data.main.temp - 273.15;`

- **Line 17**  
  **_Runtime error_**: converting the output to be integer.  
  Found it in the display where I got the result decimal number

  `let temp = data.main.temp - 273.15;` => `let temp = Math.round(data.main.temp - 273.15);`

- **Line 28 - 37**  
  **_Logical error_**: Conditions don’t get the right results.  
  Using debugger and trying cities with different temperatures.

  Incorrect Condition:

  ```
  if (temp > 0) {
  messageEl.textContent = 'Winter is coming...';
  } else if (temp > 0) {
  messageEl.textContent = 'Sweater weather!';
  } else if (temp > 10) {
  messageEl.textContent =
  'Put a jacket on and regret it as soon as you start moving';
  } else if (temp > 20) {
  messageEl.textContent = "Hotter outside than Taylor Swift's latest single";
  }
  ```

  Correct Condition:

  ```
  if (temp < 0) {
    messageEl.textContent = "Winter is coming...";
  } else if (temp >= 0 && temp <= 10) {
    messageEl.textContent = "Sweater weather!";
  } else if (temp > 10 && temp <= 20) {
    messageEl.textContent =
      "Put a jacket on and regret it as soon as you start moving";
  } else if (temp > 20) {
    messageEl.textContent = "Hotter outside than Taylor Swift's latest single";
  }
  ```
