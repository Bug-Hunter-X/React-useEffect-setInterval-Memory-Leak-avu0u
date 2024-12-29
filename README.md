# React useEffect setInterval Memory Leak

This repository demonstrates a common React bug involving memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides the corrected version.

**Problem:** The `setInterval` function continues running even after the component unmounts, leading to a memory leak.  This is because the cleanup function in `useEffect` is not used to stop the interval.

**Solution:** A cleanup function is added to `useEffect` to use `clearInterval` before the component unmounts, preventing the memory leak.

This example highlights the importance of proper cleanup in `useEffect` when using asynchronous operations such as timers.