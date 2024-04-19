#### Simple Color Generator
This is a simple color generator application built using React, JavaScript, HTML, and CSS. 
The application allows users to generate a list of shades of a specific color based on user input.

#### Features
Color Input: Users can input a color in hexadecimal format (e.g., #f15025) into the text input field.
Color Generation: Upon submitting the color input, the application generates a list of ten shades of the provided color.
Clipboard Copy: Users can click on any color to copy its hexadecimal value to the clipboard.
Error Handling: The application provides error handling for invalid color inputs.

#### How to Use
Input Color: Enter a color in hexadecimal format (e.g., #f15025) into the text input field.
Submit: Click the "submit" button to generate shades of the entered color.
Copy Color: Click on any color to copy its hexadecimal value to the clipboard.
View Shades: View the generated shades of the entered color below the input field.

#### Project Structure
App.js: The main component of the application responsible for managing state, handling user input, and rendering the color generator interface.
SingleColor.js: Component responsible for rendering individual color shades and handling clipboard copy functionality.
utils.js: Utility functions to convert RGB values to hexadecimal format.