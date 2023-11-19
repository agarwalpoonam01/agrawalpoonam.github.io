---
layout: post
title: "Error Handling in Golang"
date: 	2023-03-13 12:50:00 +0300
tags: Error 
category: Tutorial
author: Poonam Agarwal
---
### What is error handling in golang

	Software will contain errors and scenarios that are not accounted for. Error handling is an important part of programming robust, reliable, and maintainable code.
	Go offers an interesting approach to errors(a type in the language):
		Errors may be passed around functions and methods
	Handling errors is part of creating robust, reliable, & trustworthy code
	Calling a method or function that could fail, one of Go’s conventions is to return an error type as its final value

	Generally no exception will be thrown within a function if something goes wrong it is up to the caller to decide what to do with the error



### UNDERSTANDING THE ERROR TYPE
	In Go, an error is a value
	The standard library declares the error interface as follows:
	
		type error interface {
	    	Error() string

	This features a single method called Error that returns a string


### Creating error object
	package main
	import (
		"errors"
		"fmt"
	)
	func main() {
		err := errors.New("Something went wrong")
		if err != nil {
			fmt.Println(err)
		}
	}

	An error is created using the New method from the errors package
	An if statement checks whether the error value was not nil
	If the value is found to not be nil, it is printed

### DON’T PANIC
	Panic - built-in function in Go - stops ordinary flow of control, begins panicking, halting the execution of the program
	Bad idea to use this, as execution stops without any alternative
	Below example demonstrates how panic is a hard stop
		package main
		import (
		    "fmt"
		)
		func main() {
		    fmt.Println("This is executed")
		    panic("Oh no. I can do no more. Goodbye.")
		    fmt.Println("This is not executed")
		}



