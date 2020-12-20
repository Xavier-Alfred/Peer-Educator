# Welcome to the 3rd week
## This week we will see the looping and branching operations.
## Also some OOP concepts in Kotlin.
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
