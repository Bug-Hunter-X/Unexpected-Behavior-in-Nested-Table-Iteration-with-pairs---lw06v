# Lua Nested Table Iteration Bug

This repository demonstrates a potential issue when using Lua's `pairs` iterator to traverse nested tables.  The `pairs` iterator does not guarantee a specific order of iteration, and modifying a table during iteration can lead to elements being skipped.

The `bug.lua` file contains code that recursively iterates a nested table using `pairs`. Under certain conditions, this can result in unexpected behavior because `pairs` may not visit all the table's elements. 

The `bugSolution.lua` file presents a corrected approach that avoids this problem.