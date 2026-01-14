# Cheatsheet for Go Commands

## Go Compiler Commands

| Command              | Description                                               |
| -------------------- | --------------------------------------------------------- |
| `go help`            | Displays help information about Go commands and packages. |
| `go run <file.go>`   | Compiles and runs a Go program from a specified file.     |
| `go build <file.go>` | Compiles the Go source code into an executable binary.    |
| `go doc <package>`   | Find more information about a package’s function.         |
| `go version`         | Shows the current version of Go installed on your system. |
| `go env`             | Displays Go environment variables.                        |
| `go install`         | Compile and install packages and dependencies.            |
| `go get`             | Add dependencies to current module and install them.      |
| `go list`            | List packages or modules.                                 |
| `go clean`           | Remove object files and cached files.                     |
| `go test`            | Test packages.                                            |

## Go Fundamentals

| Command                              | Description                                    |
| ------------------------------------ | ---------------------------------------------- |
| `\\`                                 | One line comment                               |
| `/* ... */`                          | Multi-line comment                             |
| `package main`                       | Define package main                            |
| `import "<package>"`                 | Import package                                 |
| `import ("<package1>" "<package2>")` | Import multiple packages                       |
| `func main() {<Function logic>}`     | Define function main to action function logic. |

## Go Data Types

| Command                               | Description                                                                                        | Zero Value       |
| ------------------------------------- | -------------------------------------------------------------------------------------------------- | ---------------- |
| `int, int8, int16, int32, int64`      | Signed Integer data type (default, 8-bits or etc)                                                  | 0                |
| `uint, uint8, uint16, uint32, uint64` | Unsigned Integers, non-negative integers, <br> higher maximum value than int equivalent            | 0                |
| `float32`, `float64`                  | Floating-point data types (32-bits or 64-bits)                                                     | 0.0              |
| `complex64, complex128`               | Deals with data that have imaginary parts                                                          | 0 + 0i           |
| `string`                              | String data type                                                                                   | "                |
| `bool`                                | Boolean data type                                                                                  | false            |
| `slice`                               | Slice data type - ordered and accessed by a numerical index like lists                             | []               |
| `array`                               | Array data type - slices but with a prespecified number of elements, <br>i.e. a fixed length slice | [0, 0, 0]        |
| `map`                                 | Map data type - key-value pairs like dictionaries                                                  | nil              |
| `struct`                              | A group of related variables                                                                       | {String 0 false} |

## Go Variables

| Command                       | Description                                                                           |
| ----------------------------- | ------------------------------------------------------------------------------------- |
| `var <var> [type] = x`        | Declare variable with value x                                                         |
| `<var> := x`                  | Short variable declaration that skips `var keyword & leave compiler to infer x's type |
| `const <constant> [type] = x` | Declare constant with value x                                                         |
| `<var> = x`                   | Assign new value x to an existing variable                                            |
| `<var> += x`                  | Variable = variable + x                                                               |
| `<var> -= x`                  | Variable = variable - x                                                               |
| `<var> *= x`                  | Variable = variable \* x                                                              |
| `<var> /= x`                  | Variable = variable / x                                                               |
| `<var>++`                     | Increment variable by 1                                                               |
| `<var>--`                     | Decrement variable by 1                                                               |
| `var x, y int = -1, 5`        | Multiple variable declaration                                                         |
| `a, b := 7, 2`                | Multiple variable declaration                                                         |
| `var name, age = "Steve", 35` | Multiple different type variables declaration                                         |
| `found, ans := true, "yes"`   | Multiple different type variables declaration                                         |
| `var x *int = &y`             | `*` Operator used for Pointer Dereferencing                                           |

**NOTE** - Short variable declarations can only be called locally in a function

## Go Fmt Package

| Command                           | Description                              | Example                                     | Output                                             |
| --------------------------------- | ---------------------------------------- | ------------------------------------------- | -------------------------------------------------- |
| `fmt.Println(<args>)`             | Print line with newline                  | `fmt.Println("I", "am", "cool")`            | I am cool                                          |
| `fmt.Print(<args>)`               | Print without newline                    | `fmt.Print("I", "am", "cool")`              | Iamcool                                            |
| `fmt.Printf("<format>", <args>)`  | Print formatted string                   | `fmt.Printf("My name is %v", name)`         | My name is Leslie                                  |
| `fmt.Sprintf("<format>", <args>)` | Return formatted string without printing | `msg := fmt.Sprintf("My name is %s", name)` | Assigns string to variable `msg`                   |
| `fmt.Scan(<args>)`                | User input assigned to argument          | `fmt.Scan(&number)`                         | Assigns user input to variable address of `number` |

### Go Fmt's Formats

| Format Specifier | Description                                      |
| ---------------- | ------------------------------------------------ |
| `%v`             | Represents the named value in its default format |
| `%T`             | Represents type of the named variable            |
| `%d`             | Expects named value to be an integer type        |
| `%f`             | Expects named value to be a floating-point type  |
| `%s`             | Expects named value to be a string type          |

## Go Functions

| Command                                                            | Description                               | Example                                                                                       |
| ------------------------------------------------------------------ | ----------------------------------------- | --------------------------------------------------------------------------------------------- |
| `func main() {`<br>` <Function logic>`<br>`}`                      | Define program's main function to action. | `func main() {`<br>`  myAge := 10`<br>`  makeMeOlder(myAge)`<br>`  fmt.Println(myAge)`<br>`}` |
| `func function(<arg> <arg's type>) {`<br>`<Function logic>`<br>`}` | Define function and its logic.            | `func makeMeOlder(age int) {`<br>`  age += 5`<br>`}`                                          |

**NOTE** - In Go, only what's written in the `main` function will run when the program is called.

## Go Conditionals

| Command                           | Description                                                       |
| --------------------------------- | ----------------------------------------------------------------- |
| `if <condition> {<logic>}`        | If statement, condition may optionally be enclosed inside `(...)` |
| `else {<logic>}`                  | Else statement                                                    |
| `else if <condition> {<logic>}`   | Else if statement for additional conditionals to if statement     |
| `var := <boolean> && <boolean>`   | AND operator, returns True if all booleans is `true`              |
| `var := <boolean> \|\| <boolean>` | OR operator, returns True if either of booleans is `true`         |
| `var := !<boolean>`               | NOT operator, returns opposite of a boolean value                 |
| `switch <variable> {}`            | Switch case                                                       |
| `case <value>:`                   | Case in switch statement                                          |
| `default:`                        | Default case in switch statement                                  |

**NOTE** - Short variables can be declared within the conditional block, ; used to separate it from the condition e.g. `if age := 55; age >= 55`

## Go Loops

| Command                                       | Description                                                                                 |
| --------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `for <condition> {}`                          | For loop                                                                                    |
| `for i := 0; i < n; i++ {}`                   | Traditional loop with syntax <br> Initial Statement; Conditional Expression; Post Statement |
| `for _, value := range <collection> {}`       | For-each loop over collection                                                               |
| `break`                                       | Exit loop                                                                                   |
| `continue`                                    | Skip to next iteration of loop                                                              |
| `for <idxkey>, value := range <array/map> {}` | Loop through each contained item in a map or array, using keyword `range`                   |

## Go Maps

| Command                                | Description                                                                                | Example                         |
| -------------------------------------- | ------------------------------------------------------------------------------------------ | ------------------------------- |
| `make(map[<key type>]<value type>)`    | Create a map                                                                               | `myMap := make(map[string]int)` |
| `myMap[<key>] = <value>`               | Add key-value pair to map                                                                  | `yourMap[newKey] = newValue`    |
| `value := myMap[<key>]`                | Retrieve value by key from map                                                             | `age := myMap["Alice"]`         |
| `yourMap[existingKey] = newValue`      | Updates existing key with new value                                                        | `myMap["Alice"] = 10`           |
| `checkedValue,isFound := yourMap[key]` | Checks if key is in the map.<br> Returns value (or the zero value if missing) and boolean. | `age, exists := ages["Alice"]`  |
| `delete(yourMap, keyValueToDelete)`    | Deletes specified key:value pair                                                           | `delete(myMap, "Alice")`        |

## Go Arrays

| Command                       | Description                                 | Example                            |
| ----------------------------- | ------------------------------------------- | ---------------------------------- |
| `var arrayName [size]<type>`  | Declare an array of specified size and type | `var numbers [5]int`               |
| `arrayName := [size]<type>{}` | Declare and initialize an array             | `numbers := [5]int{1, 2, 3, 4, 5}` |
| `arrayName[index]`            | Access element at specified index           | `firstNumber := numbers[0]`        |
| `arrayName[index] = value`    | Update element at specified index           | `numbers[0] = 10`                  |
| `len(arrayName)`              | Get length of the array                     | `length := len(numbers)`           |

**NOTE** - In Go, arrays are passed into functions by value, which means that changes remain local to the function. To modify an array within a function, it must be converted into a slice.

## Go Slices

| Command                                | Description                          | Example                                                     |
| -------------------------------------- | ------------------------------------ | ----------------------------------------------------------- |
| `var sliceName []<type>`               | Declare a slice of specified type    | `var numberSlice [5]int`                                    |
| `sliceName := []<type>{}`              | Declare and initialize a slice       | `names := []string{"Kathryn", "Martin", "Sasha", "Steven"}` |
| `sliceName = append(sliceName, value)` | Append value to the end of the slice | `names = append(name, "Moh")`                               |
| `sliceName[index]`                     | Access element at specified index    | `firstElement := elementSlide[0]`                           |
| `sliceName[index] = value`             | Update element at specified index    | `names[0] = "Alex"`                                         |
| `length := len(sliceName)`             | Length of Slice                      | `noStudents := len(class)`                                  |
| `capacity := cap(sliceName)`           | Capacity of a slice                  | `classCapacity := cap(class)`                               |

**NOTE** - In Go, slices, which are pointers, are passed by reference so changes affect the original variable.

## Go Structs

| Command                         | Description                             | Example                                                         |
| ------------------------------- | --------------------------------------- | --------------------------------------------------------------- |
| `type <StructName> struct {}`   | Define a struct type                    | `type Person struct {`<br>`  Name string`<br>`  Age int`<br>`}` |
| `<structVar> := <StructName>{}` | Create and initialize a struct variable | `p := Person{Name: "Alice", Age: 30}`                           |
| `<structVar>.<fieldName>`       | Access struct field                     | `personName := p.Name`                                          |
| `<structVar>.<fieldName> = x`   | Update struct field                     | `p.Age = 31`                                                    |

## Go Pointers

| Command             | Description                                  | Example         |
| ------------------- | -------------------------------------------- | --------------- |
| `var ptr *<type>`   | Declare a pointer variable of specified type | `var ptr *int`  |
| `ptr = &<variable>` | Assign address of variable to pointer        | `ptr = &number` |
| `<variable> = *ptr` | Dereference pointer to get value             | `number = *ptr` |
| `*ptr = x`          | Update value at pointer's address            | `*ptr = 20`     |
