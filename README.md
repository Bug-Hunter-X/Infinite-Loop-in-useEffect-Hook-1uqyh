# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The example showcases an infinite loop caused by a missing dependency array, leading to continuous component re-renders.

## Bug Description

The `useEffect` hook in the provided `MyComponent` function lacks a dependency array. As a result, the effect runs after every render, incrementing the count and causing an infinite render cycle. The browser's performance will suffer and may crash depending on browser performance.

## Solution

The solution involves correctly specifying the dependency array in the `useEffect` hook. By providing an empty array `[]` the effect will only run once after the initial render.