# Understanding Questions:
1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code excutes for each step.
* The user presses the 1 button.
* A synthetic event is created
* The synthetic event is referenced by the event handler constructed in the onClick attribute of the CalcButton component whose value={1}.
* This event handler calls the dispatch function, passing in the action creator "addOne".
* addOne references the addOne handler in our actions/index.js file, which has an action type of "ADD_ONE".
* this action is being passed into our reducer in the reducers/index.js file.
* const reducer has action.type passed into a switch statement.
* because the action.type for addONE is "ADD_ONE" the switch statement evaluates the statement nested within the case "ADD_ONE".
* this statement takes the current state.total and adds 1 to it.  
* TotalDisplay shows the total plus 1.
