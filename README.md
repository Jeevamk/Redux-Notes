# `Redux Notes`
<hr>
# What is redux?
- Redux is a pattern and library for managing and updating  application state , using events called 'actions'. <br>
- It serve as a centralized store for state that need to be used across the  entire the application.<hr>

# why should use Redux?
- It helps to manage "global" state.<br>
- The patterns and tools provided by redux make it easier to understand when, where,why and how the state in your application is 
  updated and how the logic will behave when those change occur. 

# When should use Redux?
- You have large amount of applicatin state that are needed many places in app.<br>
- The state is updated frequently over time.<br>
- The logic to update the state is complex.<br>
- The app has medium or large-sized codebase,and many people worked on that app.

# React Libraries & Tools:
1) React-Redux : It is a package that react component interact with redux store by reading piece of state and dispatching an action to update the store.<br>
2) Redux-Toolkit : It a recommended approach to write redux logic.It contain functions and packages that are essential for build  
  a redux app.<br>
3) Redux Devtools extensions : It shows the history of changes to the state of your redux store over time.It allows you to dubug 
   the application effectivly. 

# Terms:
1) Action : Action is a plane javascript object that has a <b>type</b>( type field should be a string that gives this action a descriptive name) field. You can think of a action as a event that describes something that happened in application.<bR>
2) Payload : An action object can have other fields with additional information about what happened. By convention, we put that information in a field called payload.<br>
3) Action creator  : It is a function that creates and return a action object. <br>
4) Reducer : It is a function that recieves a current state and action , and decides how to update the state and it return a new state.<br>
<b>(state, action) => newState</b><br>
we can think reducers has a event listners which handle the events based on received action type.<br>
5) Store : The current redux application state lives in a object called store.<br>
6) Dispatch : The redux store has a method called dispatch.<br>
- It is the only way to update the state is to call store.dispatch() and pass in a action object.<br>
- It act like triggering a event.<br>
7) Selectors : Selectors are functions that know how to extract specific pieces of information from a store state value. As an application grows bigger, this can help avoid repeating logic as different parts of the app need to read the same data.

# Data flow
- State describe a condition of a app at a specific point in a time.<br>
- The UI is rendered based on the state.<br>
- When something happens (such as a user clicking a button), the state is updated based on what occurred.<br>
- The UI re-renders based on the new state.<br>

# slice
- A "slice" is a collection of Redux reducer logic and actions for a single feature in your app, typically defined together in a single file. The name comes from splitting up the root Redux state object into multiple "slices" of state.
