# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example shows an infinite loop caused by an improperly defined dependency array.

## Bug Description

The `useEffect` hook is used to perform side effects after a component renders. However, if the dependency array is missing or incorrect, it can lead to an infinite loop.

In this example, the `useEffect` hook is missing the dependency array `[count]`.  This means that the effect runs after every render, regardless of whether the `count` state has changed. This leads to an infinite loop as the `setCount` function changes `count`, which triggers a re-render, causing the effect to run again, ad infinitum.