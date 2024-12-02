# React Native FlatList Performance Issue with Large Datasets

This repository demonstrates a performance issue encountered when using FlatList in React Native with large datasets.  The app occasionally becomes unresponsive or experiences significant lag when rendering a large number of items.  This issue is intermittent and difficult to consistently reproduce.

## Description

The provided code uses a simple FlatList to render a list of items fetched from an API.  When the dataset is large, the app may experience performance degradation.  The issue likely stems from the way FlatList handles rendering and memory management with a substantial number of items.

## Solution

The solution file (bugSolution.js) demonstrates several strategies for improving the performance of FlatList with large datasets. These include:

* **Pagination:** Fetching and rendering only a subset of data at a time.
* **Virtualization:** Only rendering the items currently visible on the screen.
* **Optimization:** Use of `estimatedItemSize` and other performance-enhancing props. 
* **Memoization**: Using `useMemo` and `React.memo` to improve performance.

Refer to the solution code for a detailed implementation of these optimizations.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npx react-native run-android` or `npx react-native run-ios` to run the app.
4. Try to load a larger dataset (you can mock one by modifying the `fetch` call to return a larger array).  Observe potential performance issues.
