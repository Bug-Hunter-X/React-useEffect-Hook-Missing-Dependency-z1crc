# React useEffect Hook Missing Dependency
This repository demonstrates a common error in React applications involving the `useEffect` hook: forgetting to include necessary dependencies in the dependency array.  This leads to unexpected behavior where the effect runs only once on mount, even when state changes would require a re-evaluation.

## Bug Description
The provided `MyComponent` uses `useEffect` to log a message whenever the component renders. However, the dependency array is empty (`[]`), meaning the effect only runs after the initial render.  As a result, state updates to `count` do not trigger another log, leading to an inaccurate representation of the component's render cycle.