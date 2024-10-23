# SDK

A simple Go package that includes a simple function. 
This package demonstrates how to create and publish a Go module on GitHub.

## Installation

To use this package, you can import it directly from GitHub:

```bash
go get github.com/kaleabbyh/sdk/mypackage@v1.0.1

Usage

```bash
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

Repository URL: https://github.com/username/repo-name

2. Initialize Go Module
```bash
go mod init github.com/username/repo-name

3. Write Your Go Code
// File: mypackage/mypackage.go

```bash
package mypackage

// Greet returns a greeting message
func Greet(name string) string {
    return "Hello, " + name
}


4. Commit and Push the Code to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/repo-name.git
git push -u origin master


5. Tag a Version (for Go Modules)

```bash
git tag v1.0.1
git push origin v1.0.1

6. Fetch the Package

```bash
go get github.com/username/repo-name/mypackage@v1.0.1
