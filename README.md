# Infinite Loop in React Component using Tailwind CSS

This repository demonstrates an uncommon bug that can occur when using useEffect hook in a React component with Tailwind CSS. The bug causes an infinite loop and crashes the application.

## Bug Description

The bug is caused by an incorrect use of the useEffect hook's dependency array.  The `setCount(count + 1)` statement within the useEffect function causes the component to re-render, which then triggers the useEffect again, leading to an infinite loop.  This is particularly problematic because it does not show up as a clear Tailwind error but is masked within the logic.

## Bug Solution

The solution is to use the correct dependency array to control when the useEffect runs. By adding `count` to the dependency array, useEffect will only run when the value of `count` changes. Then it stops infinite loops by managing updates appropriately.