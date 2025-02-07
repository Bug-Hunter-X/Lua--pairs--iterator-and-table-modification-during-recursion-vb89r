# Lua `pairs` Iterator and Table Modification During Recursion

This repository demonstrates a potential issue in Lua involving the `pairs` iterator and modification of tables during recursion.

The `bug.lua` file contains a function that recursively iterates through a table using `pairs`.  If the function modifies the table while iterating, the `pairs` iterator may skip entries, leading to unexpected behavior.

The `bugSolution.lua` file offers a solution to the problem by using a copy of the table for iteration, preventing unintended side effects.

## How to Reproduce the Bug

1.  Run `bug.lua`.
2.  Observe that it might skip some elements, but not always.