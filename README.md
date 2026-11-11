# Exp 10 – React Strict Mode

## NAME: V.S.SREE VIVEKA  
## REG NO: 2305001031 

## Aim
To create a React application using Strict Mode and understand how it helps identify potential problems and unexpected side effects during development.

## Objectives
- To understand React Strict Mode.
- To enable Strict Mode in a React application.
- To observe the additional development-time checks.
- To understand the use of `useEffect()` and cleanup functions.

## Program

### 1. main.jsx

```jsx
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import App from "./App.jsx";

createRoot(document.getElementById("root")).render(
  <StrictMode>
    <App />
  </StrictMode>
);
```

### 2. App.jsx

```jsx
import { useEffect, useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log("Effect started");

    return () => {
      console.log("Effect cleanup");
    };
  }, []);

  return (
    <div>
      <h1>React Strict Mode</h1>

      <h2>Count: {count}</h2>

      <button onClick={() => setCount(count + 1)}>
        Increase
      </button>
    </div>
  );
}

export default App;
```

## Output

### 1. React Strict Mode Application

<img width="955" height="191" alt="WhatsApp Image 2026-11-04 at 9 02 54 PM" src="https://github.com/user-attachments/assets/e5c5db9f-3578-4813-b475-bf8fa02892fd" />

### 2. Browser Console Output

<img width="917" height="92" alt="WhatsApp Image 2026-11-04 at 9 03 53 PM" src="https://github.com/user-attachments/assets/b3747280-63fc-4fc8-9244-efbe1c70614a" />

## Result
Thus, the React application was successfully executed using Strict Mode. Its development-time checks and the use of `useEffect()` cleanup were studied.
