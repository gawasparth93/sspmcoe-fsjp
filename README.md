# SSPMCOE-FSJP

HRD

## Overview
This repository contains the source files and related resources for the SSPMCOE-FSJP project.

## Project Description
The project is currently identified with the description: `hrd`.

## Repository Structure
- `README.md` — project overview and documentation
- Additional project files and folders will be added as the project evolves

## Getting Started
1. Clone the repository.
2. Navigate to the project directory.
3. Review the available files and begin development or documentation updates.

## Notes
This README serves as the initial project documentation and can be expanded as the repository grows.

To create a Single Page Website using React concepts such as Hooks, State, Props, and Router. 
  
STEP 1: Check Node.js Installation 
Open Command Prompt or the VS Code Terminal. 
Run: 
node --version Then: 
npm --version 
If both commands show version numbers, Node.js and npm are installed. 
Example: 
v22.x.x 
10.x.x 
  
STEP 2: Create a React Project 
Open VS Code. 
Go to: 
Terminal → New Terminal 
Run: npm create vite@latest react-single-page 
You will get some options. 
Select: 
Project name: react-single-page 
 
Framework: React 
 
Variant: JavaScript 
  
STEP 3: Go Inside the Project 
Run: cd react-single-page 
Now we are inside our React project. 
  
STEP 4: Install React Packages 
Run: 
npm install 
This installs all the packages required by the React project. 
  
STEP 5: Install React Router 
We need Router for navigation. 
Run: 
npm install react-router-dom 
What is React Router? 
React Router allows us to navigate between different views/pages of a React application. 
For our practical: 
Home 
About 
Contact will be connected using Router. 
  
STEP 6: Open the Project in VS Code 
If the project is not already open, run: 
code . 
Your project will look approximately like: 
react-single-page 
│ 
├── node_modules 
├── public 
│ 
├── src 
│   ├── assets 
│   ├── App.jsx 
│   ├── App.css 
│   ├── index.css 
│   └── main.jsx 
│ 
├── package.json 
└── index.html 
For this practical, we mainly need: 
src 
 └── App.jsx 
  
STEP 7: First Understand State 
Before making the complete website, let's understand State. 
Open: 
src → App.jsx 
Delete the existing code. 
Write: 
import { useState } from "react"; 
 
function App() { 
 
  const [count, setCount] = useState(0); 
 
  return ( 
    <div> 
 
      <h1>Counter</h1> 
 
      <h2>Count: {count}</h2> 
 
      <button onClick={() => setCount(count + 1)}> 
        Increase 
      </button> 
 
    </div> 
  ); 
} 
 
export default App; 
Save the file. 
  
STEP 8: Run the Project 
In the terminal: npm run dev 
You will get something like: 
Local: http://localhost:5173/ Open that URL in your browser. 
You will see: 
Counter 
 
Count: 0 
 
[ Increase ] 
Click Increase. 
You will get:
Count: 1 
Click again: 
Count: 2 
  
STEP 9: Understand State 
Look at: 
const [count, setCount] = useState(0); 
There are three things here: 
count 
This stores the current value. 
setCount 
This changes the value. 
0 
This is the initial value. 
So: 
Initial 
count = 0 
 
      ↓ 
 
Click button 
 
      ↓ 
 
setCount(count + 1) 
 
      ↓ 
 
count = 1 
What is State? 
State is data that can change during the execution of a React component. 
  
STEP 10: Understand Hook 
We wrote: 
import { useState } from "react"; and: 
useState(0) useState() is a React Hook. 
What is a Hook? 
A Hook is a special React function that allows functional components to use React features. 
For this practical, we use: 
useState() to manage State. 
Therefore: 
Hook 
  ↓ 
useState() 
  ↓ 
State 
  ↓ 
State changes 
  ↓ 
UI updates 
  
STEP 11: Understand onClick 
We have: 
<button onClick={() => setCount(count + 1)}> 
onClick is used to detect a button click. 
When the user clicks: 
Button Click 
     ↓ 
setCount() 
     ↓ 
count increases 
     ↓ 
Screen updates 
  
STEP 12: Now Create a Props Example 
Now we will understand Props. Change App.jsx temporarily to: 
function Welcome(props) { 
 
  return ( 
    <h2> 
      Welcome, {props.name}! 
    </h2> 
  ); 
} 
 
function App() { 
 
  return ( 
    <div> 
 
      <h1>My React Website</h1> 
 
      <Welcome name="Student" /> 
 
    </div> 
  ); 
} 
 
export default App; Save the file. 
The browser shows: 
My React Website 
 
Welcome, Student! 
  
STEP 13: Understand Props 
We created: 
function Welcome(props) The component receives props. 
Then: 
<Welcome name="Student" /> passes: 
name = Student 
The Welcome component receives it through: props.name 
So: 
App Component 
      ↓ 
name="Student" 
      ↓ 
Welcome Component 
      ↓ 
props.name 
      ↓ 
Welcome, Student! 
What are Props? 
Props are used to pass data from one component to another component. 
  
STEP 14: Now Create the Home Component 
Now we will create our actual website. 
Replace App.jsx with the following code. 
First create the Home component: 
function Home() { 
 
  return ( 
    <div> 
 
      <h1>Home Page</h1> 
 
      <p> 
        Welcome to our React Single Page Website. 
      </p> 
 
    </div> 
  ); 
} 
Here: 
function Home() is a React Component. 
  
STEP 15: Create the About Component 
Below the Home component, write: 
function About() { 
 
  return ( 
    <div> 
 
      <h1>About Page</h1> 
 
      <p> 
        This website is created using React. 
      </p> 
 
    </div> 
  ); 
} 
Now we have: 
Home Component 
About Component 
  
STEP 16: Create the Contact Component 
Add: 
function Contact() { 
 
  return ( 
    <div> 
 
      <h1>Contact Page</h1> 
 
      <p> 
        Email: student@example.com 
      </p> 
 
    </div> 
  ); 
} 
Now: 
Home 
About Contact are our three components. 
  
STEP 17: Add State to Home 
Now we will combine State + Hook with our Home component. 
Change the Home component to: 
function Home() { 
 
  const [count, setCount] = useState(0); 
 
  return ( 
    <div>
 
      <h1>Home Page</h1> 
 
      <p> 
        Welcome to our React Single Page Website. 
      </p> 
 
      <h2>Counter: {count}</h2> 
 
      <button onClick={() => setCount(count + 1)}> 
        Increase 
      </button> 
 
    </div> 
  ); 
} 
Remember that we need: 
import { useState } from "react"; at the top. 
  
STEP 18: Create Props Component 
Now create: 
function Welcome(props) { 
 
  return ( 
    <h2> 
      Welcome, {props.name}! 
    </h2> 
  ); 
} 
We will pass the name later. 
  
STEP 19: Import Router 
At the very top of App.jsx, write: 
import {
  BrowserRouter, 
  Routes, 
  Route, 
  Link 
} from "react-router-dom"; 
 
import { useState } from "react"; 
What are these? 
BrowserRouter 
BrowserRouter 
Enables routing in our React application. 
Routes 
Routes 
Contains all routes. 
Route 
Route 
Defines which component should be displayed for a particular URL. 
Link 
Link 
Creates navigation links. 
  
STEP 20: Create the Main App 
Now create: 
function App() { 
 
  return ( 
 
    <BrowserRouter> 
 
      <nav> 
 
        <Link to="/">Home</Link> 
 
        {" | "} 
 
        <Link to="/about">About</Link> 
 
        {" | "} 
 
        <Link to="/contact">Contact</Link> 
 
      </nav> 
 
      <Welcome name="Student" /> 
 
      <Routes> 
 
        <Route           path="/" 
          element={<Home />} 
        /> 
 
        <Route           path="/about"           element={<About />} 
        /> 
 
        <Route           path="/contact"           element={<Contact />} 
        /> 
 
      </Routes> 
 
    </BrowserRouter> 
  ); 
} 
  
STEP 21: Complete App.jsx 
Now your complete file should be: 
import { 
  BrowserRouter, 
  Routes, 
  Route, 
  Link 
} from "react-router-dom"; 
 
import { useState } from "react"; 
 
 
function Home() { 
 
  const [count, setCount] = useState(0); 
 
  return ( 
    <div> 
 
      <h1>Home Page</h1> 
 
      <p> 
        Welcome to our React Single Page Website. 
      </p> 
 
      <h2>Counter: {count}</h2> 
 
      <button onClick={() => setCount(count + 1)}> 
        Increase 
      </button> 
 
    </div> 
  ); 
} 
 
 
function About() { 
 
  return ( 
    <div> 
 
      <h1>About Page</h1> 
 
      <p> 
        This website is created using React. 
      </p> 
 
    </div> 
  ); 
} 
 
 
function Contact() { 
 
  return (     <div> 
 
      <h1>Contact Page</h1> 
 
      <p> 
        Email: student@example.com 
      </p> 
 
    </div> 
  ); 
} 
 
 
function Welcome(props) { 
 
  return ( 
    <h2> 
      Welcome, {props.name}! 
    </h2> 
  ); 
} 
 
 
function App() { 
 
  return ( 
 
    <BrowserRouter> 
 
      <nav> 
 
        <Link to="/">Home</Link> 
 
        {" | "} 
 
        <Link to="/about">About</Link> 
 
        {" | "} 
 
        <Link to="/contact">Contact</Link> 
 
      </nav> 
 
      <Welcome name="Student" /> 
 
      <Routes> 
 
        <Route           path="/" 
          element={<Home />} 
        /> 
 
        <Route           path="/about"           element={<About />} 
        /> 
 
        <Route           path="/contact"           element={<Contact />} 
        /> 
 
      </Routes> 
 
    </BrowserRouter> 
  ); 
} 
 
 
export default App; 
  
STEP 22: Save and Run 
Save: 
Ctrl + S 
If the development server is already running, the browser will automatically update. 
Otherwise: npm run dev 
Open: 
http://localhost:5173/ 
  
STEP 23: Test Home Page 
You should see: 
Home | About | Contact 
 
Welcome, Student! 
 
Home Page 
 
Welcome to our React Single Page Website. 
 
Counter: 0 
 
[ Increase ] 
Click Increase. 
Counter: 1 
Click again: 
Counter: 2 
Here we used: 
useState() 
     ↓ 
State 
     ↓ 
setCount() 
     ↓ 
UI updates 
So this demonstrates Hook + State. 
  
STEP 24: Test Props 
At the top of the page: 
Welcome, Student! 
This comes from: 
<Welcome name="Student" /> and: 
props.name 
So this demonstrates Props. 
  
STEP 25: Test Router 
Click: 
About 
The URL changes to: 
/about 
The screen displays: 
About Page 
 
This website is created using React. 
Now click: 
Contact 
The URL becomes: 
/contact 
Output: 
Contact Page 
 
Email: student@example.com 
This demonstrates Router. 
  
STEP 26: Understand the Complete Working 
When the website starts: 
App 
 ↓ 
BrowserRouter 
 ↓ 
Navigation 
↓ 
Routes 
When Home is selected: 
/  
↓ 
Home Component 
↓ useState() ↓ 
Counter 
When About is selected: 
/about 
↓ 
About Component 
When Contact is selected: 
/contact 
↓ 
Contact Component 
Props work separately: 
App 
 ↓ 
<Welcome name="Student" /> 
 ↓ 
Welcome Component 
 ↓ 
props.name 
 ↓ 
Welcome, Student! 
  
STEP 27: Final Concept Summary 
1. Component 
A reusable building block of a React application. 
Example: 
function Home() {   return <h1>Home Page</h1>; }
2.	State 
Stores data that can change. 
const [count, setCount] = useState(0); 
3.	Hook 
A special React function. 
Example: useState() 
4.	Props 
Used to pass data between components. 
<Welcome name="Student" /> 
5.	Router 
Used to navigate between different views/pages. 
<Route path="/about" element={<About />} /> 
6.	Link 
Used to create navigation. 
<Link to="/about">About</Link> 
  
Final Output 
------------------------------------------------           React Single Page Website 
------------------------------------------------ 
 
Home | About | Contact 
 
Welcome, Student! 
 
Home Page 
 
Welcome to our React Single Page Website. 
Counter: 2 
 
[ Increase ] 
------------------------------------------------ 
When About is clicked: 
About Page 
 
This website is created using React. 
When Contact is clicked: 
Contact Page 
 
Email: student@example.com 
  
Result 
Thus, a Single Page Website was successfully created using React with Hooks, State, Props, and Router. 
 
