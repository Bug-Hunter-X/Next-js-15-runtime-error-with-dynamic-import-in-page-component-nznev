# Next.js 15 Runtime Error with Dynamic Import in Page Component

This repository demonstrates a runtime error encountered when using dynamic `import()` statements within a Next.js 15 page component.  The issue arises because the dynamic import is not handled correctly, leading to an unexpected error.  This is especially problematic because Next.js's error boundaries don't seem to catch this specific type of error.

## Bug Description
The `about.js` file attempts to dynamically import `./data.json`.  This results in a runtime error in the browser because the promise returned by the dynamic import isn't handled asynchronously.  The error is not caught, breaking the application.

## Solution
The provided solution in `aboutSolution.js` addresses this by correctly handling the promise returned from the dynamic import using `async/await`.
