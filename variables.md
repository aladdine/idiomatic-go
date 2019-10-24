# Variables

## Names

Go programmers typically use short variable names when the scope of the variable is small \(e.g. a variable inside a function\). However, if the scope is broad \(i.e. a function that is meant to be imported from another package\), longer and more meaningful names are used.

This pattern can be seen in the \(bufio\)\[[https://golang.org/src/bufio/bufio.go](https://golang.org/src/bufio/bufio.go)\] Go package.

## Scope

There are three scopes in Go:

* Local to a function: all names declared inside a function are accessible within the boundaries of the function.
* Local to a package: all names declared outside a function that start with an underscore or a lowercase letter are accessible within the package boundaries even if a package has multiple files.
* Global: all names declared outside a function that start with an uppercase letter are accessible from outside the package when the package is imported.

