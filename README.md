# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The `useEffect` hook, when used without specifying dependencies, will run after every render, potentially leading to unexpected behavior, infinite loops, and performance issues.

## Bug Description
The provided code uses `useEffect` without the `[]` dependency array. This causes it to re-run after every render, creating an infinite loop because the `setCount` function itself triggers a re-render.

## Bug Solution
The solution involves correctly specifying the dependencies array to control when the `useEffect` runs.  In this case, we only need the effect to run when the `count` changes.