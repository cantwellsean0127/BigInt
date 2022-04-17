# BigInt
Golang file used when working with numbers outside the ranges of built-in data types

Module Name: BigInt
Module Version: 1.0 (major update 1, minor update 0)
Module Release Date: Sunday, April 17th, 2022 09:40 Pacific Standard Time
Go Version: go1.17 linux/amd64
Module Author: Sean Cantwell

Purpose: Creates a BigInt type, which is used to work with numbers that exceed the ranges for built-in data types.

Module Installation: This module is designed to be open source and editable by an end user. As such the module is not treated as a module would normally be treated in go. To use this module, simpy change the package declaration so that the package name is the same as the package for which the go file you want to use this module is in; most of the time, this will be the main package. Then when running or building your code, simply add this module file to the list of files to compile.

Documentation: Currently, there is no documentation for this module, however, the documentation is a work in progress and will be released soon.

Note:  All functions that return a BigInt type, pass pointers, not copies. Please, keep this in mind whenever writing your code. This should not cause any problems as long as you don't try big_int := other_big_int and then treat the two variables as seperate. They're pointers, so under the hood, both variables actually point to the same memory address. If you need to get a copy of a BigInt, then work with the copy seperate from the original and vice versa, please use big_int.GetCopy(). Functions such as Add, Subtract, Multipy, Divide, and etc all call NewBigInt() when declaring their return values, so you CAN do product := big_int.Multiply(other_big_int) and then treat the product variable as seperate from the other two variables.
