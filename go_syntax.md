In this section, we will discover that Go file consists of the following parts namely:

Package declaration
Import packages
Functions
Statements and expressions

Let's use the code below for a better understanding

```GO
package main

import ("fmt")

func main() {
  fmt.Println("Hello World!")
}
```

// Example explained

Line 1: In Go, every program is part of a package. We define this using the package keyword. In this example, the program belongs to the main package.

Line 2: import ("fmt") lets us import files included in the fmt package.

Line 3: A blank line. Go ignores white space. Having white spaces in code makes it more readable.

Line 4: func main() {} is a function. Any code inside its curly brackets {} will be executed.

Line 5: fmt.Println() is a function made available from the fmt package. It is used to output/print text. In our example it will output "Hello World!".

Note: In Go, any executable code belongs to the main package.

// STATEMENTS IN GO

In Go, all statements are seperated by ending(Enter key) a line or by a semicolon(;)

Note: Hitting the Enter key adds ";" to the end of the line implicitly (meaning the semicolon is there but not shown physically).

The left curly bracket { cannot come at the start of a line.

// Example
```GO
package main

import ("fmt")

func main()
{
  fmt.Println("Hello World!")
}
```
This code throws an error message.

// Go Compact Code
You can write more compact code, like shown below (this is not recommended because it makes the code more difficult to read):

// Example
```GO
package main; import ("fmt"); func main() { fmt.Println("Hello World!");}
```
