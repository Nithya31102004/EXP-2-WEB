# EXPERIMENT 2: REACT LAB EXERCISE – USING PROPS

**Name:** NITHYA T  
**Register Number:** 2305001023  
**Department:** CSE

## 1. AIM

To create a React application that demonstrates how to pass data from a parent component to a child component using Props.

## 2. ALGORITHM

1. Start the program.
2. Create a React project using Vite.
3. Open the project in VS Code and identify App.jsx and the src folder.
4. Create Employee.jsx as a child component.
5. Define props for employee name, employee ID, department, and designation.
6. In App.jsx, import the Employee component.
7. Pass employee details from App.jsx to Employee.jsx using props.
8. Add three Employee components with different values.
9. Add CSS in App.css to display each employee in a separate card.
10. Run the application using npm run dev.
11. Open the localhost URL and verify that all employee details are displayed correctly.
12. Stop the program.

## 3. PROJECT STRUCTURE

```text
Experiment_02/
├── index.html
├── package.json
└── src/
    ├── main.jsx
    ├── App.jsx
    ├── App.css
    ├── index.css
    └── Employee.jsx
```

## 4. PROGRAMS

### Program 1: Employee.jsx

**Location:** `src/Employee.jsx`

```jsx
import './App.css'

function Employee({ name, id, department, designation }) {
  return (
    <div className="employee">
      <h2>Employee Details</h2>
      <p>Name: {name}</p>
      <p>ID: {id}</p>
      <p>Department: {department}</p>
      <p>Designation: {designation}</p>
    </div>
  )
}

export default Employee
```

### Program 2: App.jsx

**Location:** `src/App.jsx`

```jsx
import Employee from './Employee'
import './App.css'

function App() {
  return (
    <div className="container">
      <h1>Employee Information</h1>

      <Employee
        name="Ravi"
        id="101"
        department="CSE"
        designation="Software Developer"
      />

      <Employee
        name="Arun"
        id="102"
        department="IT"
        designation="System Engineer"
      />

      <Employee
        name="Priya"
        id="103"
        department="AIDS"
        designation="Data Analyst"
      />
    </div>
  )
}

export default App
```

### Program 3: App.css

**Location:** `src/App.css`

```css
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  background: #f4f7fb;
  color: #222;
}

.container {
  min-height: 100vh;
  text-align: center;
  padding: 40px 20px;
}

.container h1 {
  margin-bottom: 30px;
  font-size: 32px;
  color: #1e3a5f;
}

.employee {
  width: 340px;
  margin: 20px auto;
  padding: 24px;
  background: white;
  border: 1px solid #dfe5ec;
  border-radius: 12px;
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.08);
  text-align: left;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.employee:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 24px rgba(0, 0, 0, 0.12);
}

.employee h2 {
  margin-top: 0;
  margin-bottom: 16px;
  padding-bottom: 10px;
  color: #2563eb;
  border-bottom: 2px solid #e5e7eb;
}

.employee p {
  margin: 10px 0;
  font-size: 16px;
  line-height: 1.6;
  color: #374151;
}
```

### Program 4: main.jsx

**Location:** `src/main.jsx`

```jsx
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App.jsx'
import './index.css'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
)
```

### Program 5: index.css

**Location:** `src/index.css`

```css
* {
  box-sizing: border-box;
}

html, body {
  margin: 0;
  min-width: 320px;
  min-height: 100%;
}
```

## 5. EXECUTION

1. Open the Experiment_02 folder in VS Code.
2. Open the terminal.
3. Install the dependencies:

```bash
npm install
```

4. Start the React application:

```bash
npm run dev
```

5. Open the localhost URL displayed in the terminal.
6. Verify that all three employee records are displayed.

## 6. BUILD CHECK

```bash
npm run build
```

## 7. OUTPUT



## 8. OBSERVATION

The application displays three employee records in separate cards. The employee information is passed from the parent component App.jsx to the child component Employee.jsx using Props.

## 9. RESULT

Thus, a React application using Props was successfully created, and employee details were passed from the parent component to the child component and displayed correctly.
