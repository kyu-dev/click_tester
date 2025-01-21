# Simple Increment Decrement in React

This is a basic React project that demonstrates the use of `useState` to create a simple counter with increment, decrement, and reset functionality.

## Features

- Increment the counter by 1.
- Decrement the counter by 1 (but not below 0).
- Reset the counter to 0.
- Display whether the current number is positive or negative.

## Prerequisites

- Basic knowledge of React and JavaScript.
- Node.js installed on your system.

## How to Run the Project

1. **Create a React App**
   ```bash
   npx create-react-app simple-counter
   cd simple-counter
   ```

2. **Replace `src/App.js` with the following code:**

   ```javascript
   import React, { useState } from "react";

   function Counter() {
     const [count, setCount] = useState(0);

     const increment = () => {
       setCount(count + 1);
     };

     const decrement = () => {
       if (count > 0) {
         setCount(count - 1);
       }
     };

     const reset = () => {
       setCount(0);
     };

     return (
       <div style={{ textAlign: "center", marginTop: "50px" }}>
         <h1>Counter: {count}</h1>
         <p>{count >= 0 ? "Positive number" : "Negative number"}</p>
         <button onClick={increment}>+1</button>
         <button onClick={decrement}>-1</button>
         <button onClick={reset}>Reset</button>
       </div>
     );
   }

   export default Counter;
   ```

3. **Run the Project**
   ```bash
   npm start
   ```

## How it Works

1. **State Management:**
   - The `count` state is managed using React's `useState` hook.
   - `setCount` is used to update the value of `count`.

2. **Event Handlers:**
   - `increment`: Increases the `count` by 1.
   - `decrement`: Decreases the `count` by 1 only if it is greater than 0.
   - `reset`: Resets the `count` to 0.

3. **Conditional Rendering:**
   - The message below the counter changes based on whether `count` is positive or negative.

## Possible Enhancements

- Prevent the counter from exceeding a specific upper limit.
- Change the color of the number based on its value (e.g., red for negative, green for positive).
- Add animations for smoother transitions.

## License

This project is open-source and free to use for educational purposes.
