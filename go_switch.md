Go switch Statement
The switch Statement
Use the switch statement to select one of many code blocks to be executed.

The switch statement in Go is similar to the ones in C, C++, Java, JavaScript, and PHP. The difference is that it only runs the matched case so it does not need a break statement.

Single-Case switch Syntax
Syntax
switch expression {
case x:
   // code block
case y:
   // code block
case z:
...
default:
   // code block
}
This is how it works:

The expression is evaluated once
The value of the switch expression is compared with the values of each case
If there is a match, the associated block of code is executed
The default keyword is optional. It specifies some code to run if there is no case match
Single-Case switch Example
The example below uses a weekday number to calculate the weekday name:

Example
package main
import ("fmt")

func main() {
  day := 4

  switch day {
  case 1:
    fmt.Println("Monday")
  case 2:
    fmt.Println("Tuesday")
  case 3:
    fmt.Println("Wednesday")
  case 4:
    fmt.Println("Thursday")
  case 5:
    fmt.Println("Friday")
  case 6:
    fmt.Println("Saturday")
  case 7:
    fmt.Println("Sunday")
  }
}
Result:

Thursday
REMOVE ADS

The default Keyword
The default keyword specifies some code to run if there is no case match:

Example
package main
import ("fmt")

func main() {
  day := 8

  switch day {
  case 1:
    fmt.Println("Monday")
  case 2:
    fmt.Println("Tuesday")
  case 3:
    fmt.Println("Wednesday")
  case 4:
    fmt.Println("Thursday")
  case 5:
    fmt.Println("Friday")
  case 6:
    fmt.Println("Saturday")
  case 7:
    fmt.Println("Sunday")
  default:
    fmt.Println("Not a weekday")
  }
}
Result:

Not a weekday

// Go Multi-case switch Statement
The Multi-case switch Statement
It is possible to have multiple values for each case in the switch statement:

Syntax
switch expression {
case x,y:
   // code block if expression is evaluated to x or y
case v,w:
   // code block if expression is evaluated to v or w
case z:
...
default:
   // code block if expression is not found in any cases
}
Multi-case switch Example
The example below uses the weekday number to return different text:

Example
package main
import ("fmt")

func main() {
   day := 5

   switch day {
   case 1,3,5:
    fmt.Println("Odd weekday")
   case 2,4:
     fmt.Println("Even weekday")
   case 6,7:
    fmt.Println("Weekend")
  default:
    fmt.Println("Invalid day of day number")
  }
}
Result:

Odd weekday