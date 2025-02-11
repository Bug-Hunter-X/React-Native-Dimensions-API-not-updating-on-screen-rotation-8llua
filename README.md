# React Native Dimensions API - Orientation Change Bug

This repository demonstrates a common bug in React Native applications related to the `Dimensions` API and screen orientation changes.  The issue arises because the `Dimensions.get('window')` method does not automatically update when the screen rotates, causing layout problems.

The `DimensionsBug.js` file shows the buggy implementation. The `DimensionsBugSolution.js` file provides the solution, using `Dimensions.addEventListener` to resolve the problem.

## Bug Description
When the screen orientation changes, the dimensions retrieved using `Dimensions.get('window')` remain the same, leading to inaccurate layout calculations and visual inconsistencies.

## Solution
The solution involves using the `Dimensions.addEventListener` to listen for changes in the screen dimensions and trigger an update of the component's state. This ensures that the layout is recalculated with the correct dimensions after each orientation change.