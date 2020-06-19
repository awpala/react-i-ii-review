### Remember

Answer these on your own, then compare answers as a group

1.  What is state?

    * A way to manage the data of the app in an object, which can be changed over time as the application runs.

2.  Where do you set initial state?

    * `this.state = { ... } ` which is set in the constructor of a class component.

3.  What method do you use to update state?

  * `.setState({ ... })`

### Understand

Discuss this question in pairs if you have a 4-person group

4.  Explain what's happening in this component.

```jsx
import React, { Component } from "react";

class LeadMentor extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questionsAnswered: 0
    };

    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({ questionsAnswered: this.state.questionsAnswered + 1 });
  }
  render() {
    <div className="lead-mentor-container">
      <h1>Tim Biles</h1>
      <h3>{this.state.questionsAnswered}</h3>
      <h3>questions answered today</h3>
      <button onClick={this.handleClick}>Increase Answers</button>
    </div>;
  }
}
```

  * Creates a class component called `LeadMentor`, which initializes the state to have value `0` in `questionsAnswered`. A clickable button increments the counter of questions answered.

### Apply

Try these on your own, but work together if you start to get stuck.

5.  Create a `Student` component that keeps track of the number of questions the student has asked, with a button that adds 1 to the total when it's clicked

6.  Now add a text input where the student can type in their questions with a button to add them to a list of questions that is displayed below the number of questions asked.

### Analyze, Evaluate, Create

Discuss these questions as a group

7.  Could your `Student` component be refactored into a functional component? Why or why not?

    * No, because it has a state.

8.  What are the pros and cons of using a class method for an event handler vs. using an arrow function inline?

    * Advantages:
      * Doesn't require binding to the function (because arrow functions have lexical binding)
    * Drawbacks:
      * Depending on the amount and/or complexity of the codebase, using arrow functions could decrease readability of the code

9.  The render() method is called every time a component's state is updated. For a text input, that means the render method is called for every keypress. Why isn't this bad for performance?

    * Just because `render` runs, doesn't mean that the *entire* DOM (or even part of it) is being re-rendered if nothing is changing (i.e., thanks to the **virtual DOM**).