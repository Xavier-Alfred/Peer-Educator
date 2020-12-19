# Welcome to 2nd week
## Packages
A source file may start with a package declaration:
>package org.example
>
>fun printMessage() { /*...*/ }
>
>class Message { /*...*/ }
>
>//....

All the contents (such as classes and functions) of the source file are contained by the package declared.
So, in the example above, the full name of printMessage() is org.example.printMessage, and the full name of Message is org.example.Message.

## Default Imports:

A number of packages are imported into every Kotlin file by default:

- kotlin.*
- kotlin.annotation.*
- kotlin.collections.*
- kotlin.comparisons.* (since 1.1)
- kotlin.io.*
- kotlin.ranges.*
- kotlin.sequences.*
- kotlin.text.*

Let's start the **BASICS** of _Kotlin_.

## Kotlin Operators:

Operators are the special symbols that perform different operation on operands. For example + and – are operators that perform addition and subtraction respectively.
Like Java, Kotlin contains different kinds of operators.
  * Arithmetic operator.
  * Relation operator.
  * Assignment operator.
  * Unary operator.
  * Logical operator.
  * Bitwise operator.

* Arithmetic Operations:

```
fun main(args: Array<String>) 
{ 
   var a = 20 var b = 4 println("a + b = " + (a + b)) 
   println("a - b = " + (a - b)) 
   println("a * b = " + (a.times(b))) 
   println("a / b = " + (a / b)) 
   println("a % b = " + (a.rem(b))) 
}
```
* Relational Operations:
```
fun main(args: Array<String>) 
{ 
   var c = 30
   var d = 40
   println("c > d = "+(c>d)) \\c > d == false
    println("c < d = "+(c.compareTo(d) < 0)) \\ c > d = true
   println("c >= d = "+(c>=d)) \\ c >= d = false
   println("c <= d = "+(c.compareTo(d) <= 0)) \\ c <= d true
   println("c == d = "+(c==d)) \\ c == d = false
   println("c != d = "+(!(c?.equals(d) ?: (d === null)))) c != d = true
} 
```
* Assignment Operators -

```
fun main(args : Array<String>){ 

var a = 10
var b = 5
a+=b 
println(a) 
a-=b 
println(a) 
a*=b 
println(a) 
a/=b 
println(a) 
a%=b 
println(a) 
} 
```

* Unary Operators -

```
fun main(args : Array<String>){ 

    var e=10

   var flag = true

   println("First print then increment: "+ e++) 

    println("First increment then print: "+ ++e) 

    println("First print then decrement: "+ e--) 

    println("First decrement then print: "+ --e) 

}
```

* Logical Operators -

```
fun main(args : Array<String>){ 

    var x = 100
    var y = 25
    var z = 10
   var result = false
    if(x > y && x > z) 
    println(x) 
   if(x < y || x > z) 
    println(y) 
    if( result.not()) 
     println("Logical operators") 

}
```
* Bitwise Operators -

```
fun main(args: Array<String>) 
{    println("5 signed shift left by 1 bit: " + 5.shl(1)) 
    println("10 signed shift right by 2 bits: : " + 10.shr(2)) 
    println("12 unsigned shift right by 2 bits:  " + 12.ushr(2)) 
    println("36 bitwise and 22: " + 36.and(22)) 
    println("36 bitwise or 22: " + 36.or(22)) 
    println("36 bitwise xor 22: " + 36.xor(22)) 
    println("14 bitwise inverse is: " + 14.inv()) 
}
```

## Expressions in **Kotlin**
An expression consists of variables, operators, methods calls etc that produce a single value. Like other language, Kotlin expression is building blocks of any program that are usually created to produce new value. Sometimes, it can be used to assign a value to a variable in a program.
It is to be noted that an expression can contain another expression.
  - A variable declaration can not be an expression.
  - Assigning a value is not an expression.
  - A class declaration is not an expression
>> Note: In Kotlin every function returns a value atleast Unit, so every function is an expression.

## Statement in **Kotlin**
A statement is the syntactic unit of any programming language that expresses some action to be carried out. A program is formed by the sequence of one or more statements. 
In Java, a statement always ends with a semicolon but, in Koltin semicolon(;) is **optional**.
  - Declaration of a variable is a statement.
      ```
      val marks = 90
      var grade = 'A'
      ```
 ### Multiple Statements in *kotlin*
 
Multiple statements are the statements when you write more than one statement in a single line.

```
fun main(args: Array<String>){ 

   val sum: Int 
    sum = 100
    println(sum)                             // single statement 
    println("Hello");println("Geeks!")       // Mutilple statements 
}
```
## Blocks in *kotlin*

A block is a section of software code enclosed with curly braces ({…}). A block can consist of one or more statements, preceded by the declarations of variables. 
A block contains one or more blocks nested within it. Every function has its own block and main function also contains a block.

```
fun main(args: Array<String>) {              //start of main block or outer block 
     val array = intArrayOf(2, 4, 6, 8) 
     for (element in array) {                // start of inner block 
        println(element) 
     }                                       // end of inner block 
 } 
```

## Now we will see the Type Casting or Type Conversion in *Kotlin*

Type conversion (also called as Type casting) refers to changing the entity of one data type variable into another data type.

As we know Java supports implicit type conversion from smaller to larger data type. An integer value can be assigned to long data type.

**In Kotlin, helper function can be used to explicitly convert one data type to another to another data type.**

* The following helper function can be used to convert one data type into another:

    * toByte()
    * toShort()
    * toInt()
    * toLong()
    * toFLoat()
    * toDouble()
    * toChar()
```
fun main(args: Array<String>) 
{ 
  
    println("259 to byte: " + (259.toByte())) \\3
    println("50000 to short: " + (50000.toShort())) \\-15536 
    println("21474847499 to Int: " + (21474847499.toInt())) \\ 11019
    println("10L to Int: " + (10L.toInt())) \\ 10
    println("22.54 to Int: " + (22.54.toInt())) \\22
    println("22 to float: " + (22.toFloat())) \\22.0
    println("65 to char: " + (65.toChar())) \\A
    println("A to Int: " + ('A'.toInt())) \\65
} 
```
