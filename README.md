# React Native: undefined is not an object (evaluating 'this.state.myVariable')

This repository demonstrates a common React Native error: attempting to access component state before it's been mounted.  The `Bug.js` file shows the problematic code.  The solution, presented in `BugSolution.js`, utilizes `componentDidMount` to ensure state is available.

## Bug Description
Accessing `this.state` or `this.props` in the constructor or before the component has fully mounted frequently results in an error similar to "undefined is not an object (evaluating 'this.state.myVariable')".

## Solution
The best solution is to perform actions dependent on the state or props within the `componentDidMount` lifecycle method. This ensures that the component has had a chance to receive its initial props and set its state before those values are accessed.