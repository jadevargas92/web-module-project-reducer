# Understanding Questions:

1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code excutes for each step.

- The user presses the 1 button.
- the onClick runs the addOneClickHandler (defined in the App Component)
- The addOneClickHandler then dispatches (which we get from useReducer) the addOne function
- The addOne function returns to the reducer an object with {type:ADD_ONE}
- Teh reducer (using Switch Case) finds its case of ADD_ONE, and it returns a new object with the initial contents of state, plus an updated total, using calculateResult.
- CalculateResult passes in 3 arguments
- since the initial value was a '+' the calculate result function uses switch case to return the case('+') which returns num1 (state.total) and num2(action.payload)

- TotalDisplay shows the total plus 1.
