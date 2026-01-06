+++
title = "React Hooks: A Practical Guide"
date = 2024-01-02T09:00:00Z
draft = false
tags = ["react", "javascript", "hooks"]
slug = "react-hooks-guide"
+++

React Hooks revolutionized how we write React components. Let's explore the most commonly used ones.
<!--more-->

## useState

Manage state in functional components:

```jsx
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```

## useEffect

Handle side effects:

```jsx
import { useEffect } from 'react';

function UserProfile({ userId }) {
  useEffect(() => {
    fetch(`/api/users/${userId}`)
      .then(res => res.json())
      .then(data => console.log(data));
  }, [userId]); // Re-run when userId changes

  return <div>User Profile</div>;
}
```

## useContext

Access context without prop drilling:

```jsx
import { useContext } from 'react';
import { ThemeContext } from './ThemeContext';

function ThemedButton() {
  const theme = useContext(ThemeContext);

  return (
    <button style={{ background: theme.background }}>
      Click me
    </button>
  );
}
```

## Custom Hooks

Create reusable logic:

```jsx
function useLocalStorage(key, initialValue) {
  const [value, setValue] = useState(() => {
    const stored = localStorage.getItem(key);
    return stored ? JSON.parse(stored) : initialValue;
  });

  useEffect(() => {
    localStorage.setItem(key, JSON.stringify(value));
  }, [key, value]);

  return [value, setValue];
}
```

Hooks make React code more reusable and easier to understand!
