

## Steps to create and publish golang package

If you'd like to set up, you can follow these steps:

1. **Create a GitHub Repository**  
   Create a new repository on GitHub:

   Repository URL: `https://github.com/username/repo-name`



2. **Initialize Go Module**  
   Run the following command:

   ```bash
   mkdir project-name
   cd project-name
   go mod init github.com/username/repo-name
   ```


3. **Write Your Go Code**  
   Create the file `mypackage/mypackage.go` with the following content:

   ```go
   package mypackage

   // Greet returns a greeting message
   func Greet(name string) string {
       return "Hello, " + name
   }
   ```


4. **Commit and Push the Code to GitHub**  
   Execute the following commands:

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/username/repo-name.git
   git push -u origin master
   ```


5. **Tag a Version (for Go Modules)**  
   Tag your version:

   ```bash
   git tag v1.0.1
   git push origin v1.0.1
   ```


6. **Fetch the Package**  
   To use the package, run:

   ```bash
   go get github.com/username/repo-name/mypackage@v1.0.1
   ```


## Installation

To use this package, you can import it directly from GitHub:

```bash
go get github.com/kaleabbyh/sdk/mypackage@v1.0.1
```

## Usage

You can use the package in your Go code as follows:

```go
package main

import (
	"fmt"

	"github.com/kaleabbyh/sdk/mypackage"
)

func main() {
	greeting := mypackage.Greet("kaleab")
	fmt.Println(greeting)
}
```