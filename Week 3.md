# Welcome to the 3rd week
## This week we will see the looping and branching operations.
## Also some function concepts in Kotlin.
# Kotlin *if-else* expression
Decision Making in programming is similar to decision making in real life. In programming too, a certain block of code needs to be executed when some condition is fulfilled.
A programming language uses control statements to control the flow of execution of program based on certain conditions.
If condition is true then it enters into the conditional block and executes the instructions.

There are different types of if-else expressions in Kotlin:

* if expression
* if-else expression
* if-else-if ladder expression
* nested if expression

### if statement:

It is used to specify a block of statements to be executed or not i.e if a certain condition is true then the statement or block of statements to be executed otherwise fails to execute.

#### Syntax

```
if(condition) {

       // code to run if condition is true
}
```

#### Example
```

fun main(args: Array<String>) { 
    var a = 3
    if(a > 0){ 
        print("Yes,number is positive") 
    } 
}
```

### if-else statement:

if-else statement contains two blocks of statements. ‘if’ statement is used to execute the block of code when the condition becomes true and ‘else’ statement is used to execute a block of code when the condition becomes false.

#### Syntax:

``` 
if(condition) { 
        // code to run if condition is true
}
else { 
       // code to run if condition is false
}
```
#### Example
```
fun main(args: Array<String>) { 
        var a = 5
        var b = 10
        if(a > b){ 
            print("Number 5 is larger than 10") 
        } 
        else{ 
            println("Number 10 is larger than 5") 
        } 
    } 
```

### if-else-if ladder expression:
Here, a user can put multiple conditions. All the ‘if’ statements are executed from the top to bottom. 
One by one all the conditions are checked and if any of the condition found to be true then the code associated with the if statement will be executed and all other statements bypassed to the end of the block. 
If none of the conditions is true, then by default the final else statement will be executed.

#### Syntax:
```
if(Firstcondition) { 
    // code to run if condition is true
}
else if(Secondcondition) {
    // code to run if condition is true
}
else{
}
```

#### Example
```
fun main(args: Array<String>) { 
     
    // create an object for scanner class 
    val reader = Scanner(System.`in`)        
    print("Enter any number: ") 
  
    // read the next Integer value 
    var num = reader.nextInt()              
    var result  = if ( num > 0){ 
        "$num is positive number"
    } 
    else if( num < 0){ 
        "$num is negative number"
    } 
    else{ 
        "$num is equal to zero"
    } 
    println(result) 
  
} 
```
### nested if expression:

Nested if statements means an if statement inside another if statement.If first condition is true then code the associated block to be executed, and again check for the if condition nested in the first block and if it is also true then execute the code associated with it. 
It will go on until the last condition is true.

#### Syntax
```
if(condition1){
            // code 1
      if(condition2){
                  // code2
      }
}
```

#### Example
```
fun main(args: Array<String>) { 
   
    // create an object for scanner class 
    val reader = Scanner(System.`in`)        
    print("Enter three numbers: ") 
  
    var num1 = reader.nextInt() 
    var num2 = reader.nextInt() 
    var num3 = reader.nextInt() 
  
    var max  = if ( num1 > num2) { 
        if (num1 > num3) { 
            "$num1 is the largest number"
        } 
        else { 
            "$num3 is the largest number"
        } 
    } 
    else if( num2 > num3){ 
        "$num2 is the largest number"
    } 
    else{ 
        "$num3 is the largest number"
    } 
    println(max) 
  
} 
```

# Kotlin *while* loop
In programming, loop is used to execute a specific block of code repeatedly until certain condition is met.
If you have to print counting from 1 to 100 then you have to write the print statement 100 times. 
But with help of loop you can save time and you need to write only two lines.

### While loop –
It consists of a block of code and a condition. First of all the condition is evaluated and if it is true then execute the code within the block. It repeats until the condition becomes false because every time the condition is checked before entering into the block. The while loop can be thought of as repeating of if statements.

#### Syntax
```
while(condition) {
           // coode to run
}
```
#### Example
```
fun main(args: Array<String>) { 
    var number = 1
  
    while(number <= 10) { 
        println(number) 
        number++; 
    } 
} 
```
# Kotlin *do-while* loop
First of the all the statements within the block is executed, and then the condition is evaluated. If the condition is true the block of code is executed again. The process of execution of code block repeated as long as the expression evaluates to true. If the expression becomes false, the loop terminates and transfers control to the statement next to do-while loop.
It is also known as post-test loop because it checks the condition after the block is executed.

#### Syntax
```
do {
      // code to run
{
while(condition)
```


# Kotlin *for* loop

In Kotlin, for loop is equivalent to foreach loop of other languages like C#. Here for loop is used to traverse through any data structure which provides an iterator. It is used very differently then the for loop of other programming languages like Java or C.

#### Syntax
```
for(item in collection) {
       // code to execute
}
```

In Kotlin, for loop is used to iterate through the following because all of them provides iterator.

* Range
* Array
* String
* Collection

## Iterate through range using for loop –
You can traverse through Range because it provides iterator. There are many ways you can iterate through Range. The in operator used in for loop to check value lies within the Range or not.
Below programs are example of traversing the range in different ways and in is the operator to check the value in the range. If value lies in between range then it returns true and prints the value.

### Iterate through range to print the values:

#### Syntax
```
fun main(args: Array<String>) 
{ 
    for (i in 1..6) { 
        print("$i ") 
    } 
} 
```

### Iterate through array using for loop –
An array is a data structure which contains same data type like Integer or String. Array can be traversed using for loop because it also provides iterator. Each array has a starting index and by default, it is 0.

There are the following you can traverse array:

- Without using Index property
- With Using Index property
- Using withIndex Library Function

### Iterate through string using for loop –
A string can be traversed using the for loop because it also provides iterator.

There are following ways to traverse the string:

- Without using Index property
- With Using Index property
- Using withIndex Library Function

### Iterate through collection using for loop –
You can traverse the collection using the for loop. There are three types of collections list, map and set.
In the listOf() function we can pass the different data types at the same time.

# Kotlin *functions*

A function is a unit of code that performs a special task. In programming, function is used to break the code into smaller modules which makes the program more manageable.

For example: If we have to compute sum of two numbers then define a fun sum().

```
fun sum(a: Int, b: Int): Int {
    return a + b
}
```
We can call sum(x, y) at any number of times and it will return sum of two numbers. So, function avoids the repetition of code and makes the code more reusable.

In Kotlin, there are two types of function-

* Standard library function
* User defined function

## Kotlin standard library function –
In Kotlin, there are different number of built-in functions already defined in standard library and available for use. We can call them by passing arguments according to requirement.

In below program, we will use built-in functions arrayOf(), sum() and println(). The function arrayOf() require some arguments like integers, double etc to create an array and we can find the sum of all elements using sum() which does not require any argument.
```
fun main(args: Array<String>) { 
    var sum = arrayOf(1,2,3,4,5,6,7,8,9,10).sum() 
  
    println("The sum of all the elements of an array is: $sum") 
} 
```
The list of different standard library functions and their use –

- sqrt() – Used to calculate the square root of a number.
- print() – Used to print a message to standard output.
- rem() – To find the remainder of one number when divided by another.
- toInt() – To convert a number to integer value.
- readline() – Used for standard input.
- compareTo() – To compare two numbers and return boolean value.

## Kotlin user-defined function –
A function which is defined by the user is called user-defined function. As we know, to divide a large program in small modules we need to define function. Each defined function has its own properties like name of function, return type of a function, number of parameters passed to the function etc.

## Creating user-defined function-
In Kotlin, function can be declared at the top, and no need to create a class to hold a function, which we are used to do in other languages such as Java or Scala.

#### Syntax
```
fun fun_name(a: data_type, b: data_type, ......): return_type  {
    // other codes
    return
}
```
#### Example
```

brightness_4
fun student(name: String , roll_no: Int , grade: Char) { 
    println("Name of the student is : $name") 
    println("Roll no of the student is: $roll_no") 
    println("Grade of the student is: $grade") 
} 
```

## Recursion in Kotlin

A function which calls itself is called as recursive function and this process of repetition is called recursion.

Whenever a function is called then there are two possibilities –

1. Normal function call
2. Recursive function call

## Recursive Function Call
When a function calls itself then it is called recursive function call. Every recursive function should have terminate condition else program executions enters in infinite loop and results into stack overflow error.

#### Example
```
// Kotlin program of factorial using recursion 
fun Fact(num: Int):Long{ 
    return  num*Fact(num-1)  // no terminate condition 
}     
//main method 
fun main() { 
    println("Factorial of 5 is: "+Fact(5)) 
//Recursive call 
} 
```

## *Collections* in Kotlin
Similar to Java Collections, Kotlin also introduced the concept of collections. A collection usually contains a number of objects of the same type and these objects in the collection are called elements or items.

Kotlin Standard Library provides a rich set of tools for managing collections.

#### Types of Collections –
In Kotlin collections are categories into two forms.

1. Immutable Collection
2. Mutable Collection

Immutable means that it supports only read-only functionalities and can not be modified its elements. Immutable Collections and their corresponding methods are:

- List – listOf() and listOf<T>()
- Set – setOf()
- Map – mapOf()

**List** – It is an ordered collection in which we can access to elements or items by using indices – integer numbers that define position for each element. Elements can be repeated in a list any number of times. We can perform add or remove operations in the immutable list.

#### Example
```
// An example for immutable list 
fun main(args: Array<String>) { 
    val immutableList = listOf("Mahipal","Nikhil","Rahul") 
    // gives compile time error  
    // immutableList.add = "Praveen" 
    for(item in immutableList){ 
        println(item) 
    } 
} 
```
**Set** – It is a collection of unordered elements also it does not support duplicate elements. It is a collection of unique elements. Generally, the order of set elements does not has significant effect. We can not perform add or remove operations because it is immutable Set.

#### Example
```
fun main(args: Array<String>) { 
    // initialize with duplicate values but output with no repeatition 
    var immutableSet = setOf(6,9,9,0,0,"Mahipal","Nikhil") 
    // gives compile time error 
    //immutableSet.add(7) 
    for(item in immutableSet){ 
        println(item) 
    } 
} 
```
**Map** – Map keys are unique and holds only one value for each key, it is a set of key-value pairs. Each key maps to exactly one value. The values can be duplicates but keys should be unique. Maps are used to store logical connections between two objects, for example, a student ID and their name. As it is immutable it’s size is fixed and it’s methods supports read-only access.

```
// An example for immutable map 
fun main(args : Array<String>) { 
    var immutableMap = mapOf(9 to "Mahipal",8 to "Nikhil",7 to "Rahul") 
    // gives compile time error 
    // immutableMap.put(9,"Praveen") 
    for(key in immutableMap.keys){ 
        println(immutableMap[key]) 
    } 
} 
```

**Mutable** Collection supports both read and write functionalities. Mutable collections and their corresponding methods are:

- List – mutableListOf(),arrayListOf() and ArrayList
- Set – mutableSetOf(), hashSetOf()
- Map – mutableMapOf(), hashMapOf() and HashMap
List – Since mutable list supports read and write operation, declared elements in the list can either be removed or added.

#### Example
```
fun main(args : Array<String>) { 
    var mutableList = mutableListOf("Mahipal","Nikhil","Rahul") 
    // we can modify the element 
    mutableList[0] = "Praveen"
    // add one more element in the list 
    mutableList.add("Abhi") 
    for(item in mutableList){ 
        println(item) 
    } 
 ```
**Set** – The mutable Set supports both read and write functionality. We can access add or remove elements from the collections easily and it will preserve the order of the elements.

```
fun main(args: Array<String>) { 
    var mutableSet = mutableSetOf<Int>(6,10) 
    // adding elements in set 
    mutableSet.add(2) 
    mutableSet.add(5) 
    for(item in mutableSet){ 
        println(item) 
    } 
} 
```

**Map** – It is mutable so it supports functionalities like put, remove, clear etc.

#### Example
```
fun main(args : Array<String>) { 
    var mutableMap = mutableMapOf<Int,String>(1 to "Mahipal",2 to "Nikhil",3 to "Rahul") 
    // we can modify the element 
    mutableMap.put(1,"Praveen") 
    // add one more element in the list 
    mutableMap.put(4,"Abhi") 
    for(item in mutableMap.values){ 
        println(item) 
    } 
} 
```
