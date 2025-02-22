# React setInterval Memory Leak
This repository demonstrates a common mistake when using the `setInterval` function within a React component's `useEffect` hook.  This improper usage can cause memory leaks.

The `bug.js` file shows the erroneous implementation where the `setInterval` function is not properly cleaned up.  This leads to a continuous counter update even after the component is unmounted.

The `bugSolution.js` file provides the correct implementation that avoids the memory leak by using a cleanup function within the `useEffect` hook to clear the interval before the component is unmounted.