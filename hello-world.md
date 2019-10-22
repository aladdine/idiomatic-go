# Hello World

```go
// Package declraration is mandatory.
// The main package is the entry point to your program.
package main

import "fmt"  // Module import.

// The main function is the entry point to the current package.
func main() {
	fmt.Println("Hello World 1!")
}
```

To run the program above, copy it to a hello\_word.go file and run:

```bash
go run hello_world.go
```

Alternative, you can build the program first then run the binary:

```bash
go build hello_world.go
./hello_world
```

