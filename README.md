# Tcl Bug: Unexpected Numeric Comparison with ==

This repository demonstrates a common, yet subtle, bug in Tcl related to the use of the `==` operator for numeric comparison.  The `==` operator in Tcl performs string comparison, which can lead to unexpected results when comparing numbers stored as strings.

## Bug Description
The `bug.tcl` file contains a procedure `buggyProc` that attempts to compare two numbers. However, due to the use of `==`, the comparison is actually string comparison, potentially causing incorrect results.

## Solution
The `bugSolution.tcl` file demonstrates how to correct this issue using the `expr` command to force a numeric comparison.

## How to Reproduce
1. Clone this repository.
2. Run `bug.tcl` and observe the unexpected output.
3. Run `bugSolution.tcl` to see the corrected behavior.

## Learning Points
* Always use the `expr` command for explicit numeric comparison in Tcl.
* Be mindful of Tcl's string-based nature when performing comparisons.