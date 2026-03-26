// GO ARRAYS

Arrays are used to store multiple values of the same type in a single variable, instead of declaring separate variables for each value.

Declare an Array
In Go, there are two ways to declare an array:

1. With the var keyword:
Syntax
```GO
var array_name = [length]datatype{values} // here length is defined
``` 

or

```GO
var array_name = [...]datatype{values} // here length is inferred
```

2. With the := sign:
Syntax
```GO
array_name := [length]datatype{values} // here length is defined
```


or

```GO
array_name := [...]datatype{values} // here length is inferred
```

Note: The length specifies the number of elements to store in the array. In Go, arrays have a fixed length. The length of the array is either defined by a number or is inferred (means that the compiler decides the length of the array, based on the number of values).

Array Examples
Example
This example declares two arrays (arr1 and arr2) with defined lengths:

```GO
package main
import ("fmt")

func main() {
  var arr1 = [3]int{1,2,3}
  arr2 := [5]int{4,5,6,7,8}

  fmt.Println(arr1)
  fmt.Println(arr2)
}
Result:

[1 2 3]
[4 5 6 7 8]
```

Example
This example declares two arrays (arr1 and arr2) with inferred lengths:

```GO
package main
import ("fmt")

func main() {
  var arr1 = [...]int{1,2,3}
  arr2 := [...]int{4,5,6,7,8}

  fmt.Println(arr1)
  fmt.Println(arr2)
}
```

Result:

[1 2 3]
[4 5 6 7 8]

Example
This example declares an array of strings:

```GO
package main

import ("fmt")

func main() {
  var cars = [4]string{"Volvo", "BMW", "Ford", "Mazda"}
  fmt.Print(cars)
}
```

Result:

[Volvo BMW Ford Mazda]


Access Elements of an Array
You can access a specific array element by referring to the index number.

In Go, array indexes start at 0. That means that [0] is the first element, [1] is the second element, etc.

Example
This example shows how to access the first and third elements in the prices array:

```GO
package main

import ("fmt")

func main() {
  prices := [3]int{10,20,30}

  fmt.Println(prices[0])
  fmt.Println(prices[2])
}
```
Result:

10
30


Change Elements of an Array
You can also change the value of a specific array element by referring to the index number.

Example
This example shows how to change the value of the third element in the prices array: 

```GO
package main

import ("fmt")

func main() {
  prices := [3]int{10,20,30}

  prices[2] = 50
  fmt.Println(prices)
}
```

Result:

[10 20 50]


Array Initialization
If an array or one of its elements has not been initialized in the code, it is assigned the default value of its type.

Tip: The default value for int is 0, and the default value for string is "".

Example
```GO
package main

import ("fmt")

func main() {
  arr1 := [5]int{} //not initialized
  arr2 := [5]int{1,2} //partially initialized
  arr3 := [5]int{1,2,3,4,5} //fully initialized

  fmt.Println(arr1)
  fmt.Println(arr2)
  fmt.Println(arr3)
}
```

Result:

[0 0 0 0 0]
[1 2 0 0 0]
[1 2 3 4 5]


Initialize Only Specific Elements
It is possible to initialize only specific elements in an array.

Example
This example initializes only the second and third elements of the array: 

```GO
package main

import ("fmt")

func main() {
  arr1 := [5]int{1:10,2:40}

  fmt.Println(arr1)
}
``` 
Result:

[0 10 40 0 0]


Example Explained
 The array above has 5 elements.

1:10 means: assign 10 to array index 1 (second element).
2:40 means: assign 40 to array index 2 (third element).
Find the Length of an Array
The len() function is used to find the length of an array:

Example

```GO
package main
import ("fmt")

func main() {
  arr1 := [4]string{"Volvo", "BMW", "Ford", "Mazda"}
  arr2 := [...]int{1,2,3,4,5,6}

  fmt.Println(len(arr1))
  fmt.Println(len(arr2))
}
```
Result:

4
6