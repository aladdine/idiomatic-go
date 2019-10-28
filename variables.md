# Variables

## Names

Go programmers typically use short variable names when the scope of the variable is small \(e.g. a variable inside a function\). However, if the scope is broad \(i.e. a function that is meant to be imported from another package\), longer and more meaningful names are used.

This pattern can be seen in the \[bufio\]\([https://golang.org/src/bufio/bufio.go](https://golang.org/src/bufio/bufio.go)\) Go package.

## Declarations

There are four types of declarations:

* const: to declare a constant.
* funct: to declare a function.
* type: to declare a struct.
* var: to declare a variable whose value may change.

#### Variable Declarations:

A var declaration followed by an arbitrary variable name and a type declares the variable and initializes it based on its type \(e.g. 0 for int, empty string for string, etc\). 

```go
var i int
```

The variable can also be initialized in the same  declaration statement.

```go
var j int = 5
```

An alternative form that uses type inference:

```go
k := 10.0
```

## Scope

There are three scopes in Go:

* Local to a function: all names declared inside a function are accessible within the boundaries of the function.
* Local to a package: all names declared outside a function that start with an underscore or a lowercase letter are accessible within the package boundaries even if a package has multiple files.
* Global: all names declared outside a function that start with an uppercase letter are accessible from outside the package when the package is imported.

### Pointers

A pointer value stores the address of a variable. Pointer variables and their types are preceded with with an asterix. The address of a variable can be retrieved by using the ampersand sign. Pointers are convenient to access variables outside of their lexical scope and also when their name is unknown.

The zero value of a pointer is `nil` and two pointers are equal if they point to the same address or both are `nil`.

```go
val := "foo"
ptr := &val
fmt.Print(*ptr)    // "foo"
*ptr := "bar"
fmt.Println(*ptr)  // "bar"# 
```

### The \`new\` Built-in Function

The  `new` keyword creates a pointer with a given type. This makes it convenient when the name of the variable is not necessary.

```go
p := new(int)
```



