# SDK

A simple Go package that includes a simple function. 
This package demonstrates how to create and publish a Go module on GitHub.

## Installation

To use this package, you can import it directly from GitHub:

```bash
go get github.com/kaleabbyh/sdk/mypackage@v1.0.1

Usage

package main

import "github.com/kaleabbyh/sdk/mypackage"

func main() {
    greeting := mypackage.Greet("Kaleab")
    println(greeting)
}


Steps to Reproduce
If you'd like to set up a similar project, follow these steps:

1. Create a GitHub Repository
Create a new repository on GitHub:

Repository URL: https://github.com/kaleabbyh/sdk

2. Initialize Go Module
go mod init github.com/kaleabbyh/sdk

3. Write Your Go Code
// File: mypackage/mypackage.go
package mypackage

// Greet returns a greeting message
func Greet(name string) string {
    return "Hello, " + name
}


4. Commit and Push the Code to GitHub
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/kaleabbyh/sdk.git
git push -u origin master


5. Tag a Version (for Go Modules)
git tag v1.0.0
git push origin v1.0.0

6. Fetch the Package
go get github.com/kaleabbyh/sdk/mypackage@v1.0.0
