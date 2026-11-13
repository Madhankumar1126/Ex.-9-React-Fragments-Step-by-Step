# Ex.-9-React-Fragments-Step-by-Step
## Name: Madhan Kumar J
## Roll no: 2305001016
## Department: CSE

## AIM
### To understand and implement React Fragments to group multiple JSX elements without creating unnecessary DOM elements.

## PROGRAM

### i) App.jsx
```jsx
import { Fragment } from "react";
import "./App.css";

function Student() {
  return (
    <>
      <h2>Student Details</h2>
      <p>Name: Ajith</p>
      <p>Department: CSE</p>
      <p>Year: III Year</p>
    </>
  );
}

function App() {
  const students = [
    { id: 1, name: "Ajith" },
    { id: 2, name: "Ravi" },
    { id: 3, name: "Divya" },
  ];

  return (
    <div className="container">
      <h1>College Information</h1>
      <Student />
      <hr />
      <h2>Student List</h2>
      {students.map((student) => (
        <Fragment key={student.id}>
          <h3>{student.name}</h3>
          <p>Department: Computer Science</p>
          <hr />
        </Fragment>
      ))}
    </div>
  );
}

export default App;
```

## OUTPUT
<img width="818" height="347" alt="image" src="https://github.com/user-attachments/assets/c564584a-ebf3-4106-9e41-03f28067d886" />
<img width="820" height="366" alt="image" src="https://github.com/user-attachments/assets/984ceab0-d4eb-4a71-a985-27aa05aa7603" />



## RESULT
### Thus, React Fragments were successfully implemented using both shorthand syntax (<> </>) and explicit Fragment syntax. Multiple JSX elements were grouped without adding extra wrapper elements to the DOM.
