### Remember

Answer these on your own, then compare answers as a group

1.  What is React?

    * An open-source JavaScript library for creating single-age applications (SPAs) using  a component-based architecture with unidirectional data flow, developed and maintained by Facebook

2.  What is create-react-app?

    * A command to create a boilerplate react app via npm, with pre-configured dependencies

3.  What is Component Based Architecture?

    * An application structure based on independently specified UI components which can interact hierarchically to confer functionality on the full app

4.  What is JSX?

    * Syntax extension, allowing to embed HTML tags within JavaScript; syntax used by React to describe a user interface

5.  What is the virtual DOM?

    * A representation of the DOM by React, allowing for dynamic behavior of the application by rendering in real-time with the page's DOM

6.  What is unidirectional (one-way) data flow?

    * The movement of data down the component hierarchy from parent to child(ren); this can be circumvented by feeding back information upwards via events 

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`

    * Creates a boilerplate app called 'my-app' with pre-configured dependencies

8.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

  * Creates a functional (state-less) component named `Mentor`, which represents a `<div>` container for the mentor entity. `props.title` is used to access the property `title` to evaluate 

9.  Explain how data is passed from a parent component to a child component.

    * By using `props`.

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?

    * Benefits:
      * Allows to bootstrap a React app quickly
      * Doesn't require installation of individual dependencies required in the React app
      * Most of the configuration is already done out of the box
    * Drawbacks:
      * It could potentially introduce bloat (i.e., unused dependencies)

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

14. Compare and contrast one-way data flow with two-way data binding.

    * One-way = uni-directional
    * Two-way = bi-directinal