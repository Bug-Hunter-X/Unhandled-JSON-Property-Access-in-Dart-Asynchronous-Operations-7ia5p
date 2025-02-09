# Unhandled JSON Property Access in Dart Asynchronous Operations

This repository demonstrates a common error in Dart code that handles asynchronous operations and JSON data: accessing a JSON property that might not exist.  The code showcases the problem and provides a solution to make the code more robust.

## Problem

The `bug.dart` file contains a function `fetchData` that fetches JSON data from a URL.  However, it attempts to access the `name` property of the JSON response without checking if it exists. If the JSON response does not contain a `name` property, this will lead to a runtime error.

## Solution

The `bugSolution.dart` file demonstrates a solution to this problem by using the following techniques:

1. **Null Safety:** Uses the `?` operator to indicate that the `name` property can be null.
2. **Null Checks:** Explicitly checks if `name` is null before using it.
3. **Default Values:** Provides a default value in case `name` is not found in the JSON response.

This approach makes the code more reliable and prevents crashes caused by unexpected JSON structures.