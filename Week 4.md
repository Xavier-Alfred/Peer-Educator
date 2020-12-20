# Welcome to 4th week
## Kotlin **Class** and **Objects**
Kotlin supports both functional and object-oriented programming. In previous articles, we have learned about functions, higher-order functions and lambdas which represents Kotlin as a functional language. Here, we will learn about the basic OOPs concepts which represent Kotlin as Object-Oriented programming language.

### Object-Oriented Programming Language –
Class and Objects are the basic concepts of object-oriented programming language. These support the OOPs concepts inheritance, abstraction etc.

## Class
Like Java, class is a blue print for the objects having similar properties. We need to define a class before creating object and class keyword is used to define a class.

The class declaration consist of class name, class header and class body enclosed with curly braces.

#### Syntax of class declaration:

```
class className {      // class header
   // property
   // member function
}
```

#### Creating constructor:
```
class className constructor(parameters) {    
   // property
   // member function
}
```
#### Example of Koltin class –

```
class employee { 
    // properties 
    var name: String = ""
    var age: Int = 0
    var gender: Char = 'M'
    var salary: Double = 0.toDouble() 
   //member functions  
   fun name(){ 
  
    } 
    fun age() { 
  
    } 
    fun salary(){ 
  
    } 
} 
```

## Object
It is a basic unit of Object Oriented Programming and represents the real-life entities, which has state and behavior. Objects are used to access the properties and member function of a class. In Kotlin, we can create multiple objects of a class. An object consists of :

**State** : It is represented by attributes of an object. It also reflects the properties of an object.
**Behavior** : It is represented by methods of an object. It also reflects the response of an object with other objects.
**Identity** : It gives a unique name to an object and enables one object to interact with other objects.

## Create an object-
We can create an object using the reference of the class.

```
var obj = className()
```

#### Accessing the property of the class-
We can access the properties of class using an object. First create an object using the class reference then access the property.

```
obj.nameOfProperty
```

#### Accessing the member function of class-
We can access the member function of the class using the object.

```
obj.funtionName(parameters)
```

```
class employee {// Constructor Declaration of Class 
  
    var name: String = ""
    var age: Int = 0
    var gender: Char = 'M'
    var salary: Double = 0.toDouble() 
  
    fun insertValues(n: String, a: Int, g: Char, s: Double) { 
        name = n 
        age = a 
        gender = g 
        salary = s 
        println("Name of the employee: $name") 
        println("Age of the employee: $age") 
        println("Gender: $gender") 
        println("Salary of the employee: $salary") 
    } 
    fun insertName(n: String) { 
        this.name = n 
    } 
  
} 
fun main(args: Array<String>) { 
    // creating multiple objects 
    var obj = employee() 
    // object 2 of class employee 
    var obj2 = employee() 
  
    //accessing the member function 
    obj.insertValues("Praveen", 50, 'M', 500000.00) 
  
    // accessing the member function 
    obj2.insertName("Aliena") 
  
    // accessing the name property of class 
   println("Name of the new employee: ${obj2.name}") 
  
} 
```
## Nested Class in Kotlin

A class is declared within another class then it is called as nested class. By default nested class is static so we can access the nested class property or variables using dot(.) notation without creating object of the class.

### Syntax of declaration:
```


class outerClass {
       ............
      // outer class properties or member function
      
      class nestedClass { 
            ..........
            // inner class properties or member function
      }
}
```
**Note**: Nested class can’t access the members of outer class, but we can access the property of nested class from the outer class without creating object for nested class.

```
// outer class declaration 
class outerClass { 
    var str = "Outer class"
    // nested class declaration 
    class nestedClass { 
        val firstName  = "Praveen"
        val lastName = "Ruhil"
    } 
} 
fun main(args: Array<String>) { 
    // accessing member of Nested class 
    print(outerClass.nestedClass().firstName) 
    print(" ") 
    println(outerClass.nestedClass().lastName) 
}     
```
### Kotlin Inner Class –

When we can declare a class inside another class using the keyword inner then it is called inner class. With the help of inner class we can access the outer class property inside the inner class.

```
class outerClass {
       ............
      // outer class properties or member function
      
      inner class innerClass { 
            ..........
            // inner class properties or member function
      }
}
```

#### Kotlin Data Classes

We often create classes to hold some data in it. In such classes, some standard functions are often derivable from the data. In Kotlin, this type of class is known as data class and is marked as data.

##### Example of a data :
```
data class Student(val name: String, val roll_no: Int)
```
The compiler automatically derives the following functions :

- equals()
- hashCode()
- toString()
- copy()

### Rules to create Data classes –
Data classes have to fulfill the following requirements to ensure the consistency:

* The primary constructor needs to have at least one parameter.
* All primary constructor parameters need to be marked as val or var.
* Data classes cannot be abstract, open, sealed or inner.
* Data classes may only implement interfaces.

### toString()
This function returns a string of all the parameters defined in the data class .

#### Example:
```
fun main(args: Array<String>)  
{ 
    //declaring a data class  
    data class man(val roll: Int,val name: String,val height:Int) 
   
    //declaring a variable of the above data class  
    //and initializing values to all parameters 
   
    val man1=man(1,"man",50) 
       
    //printing all the details of the data class 
    println(man1.toString()); 
} 
```
### copy()
Sometimes we need to copy an object, with some change in some of its properties keeping all others unchanged.
In this case copy() function is used.

#### Properties of copy()

- It copies all arguments or members defined in primary constructor
- Two objects can have same primary parameter values and different class body values if defined
- Declaration of copy()
```
fun copy(name: String = this.x, age: Int = this.y) = user(x, y)
```
where user is a data class : user(String, Int) .

#### Example
```
fun main(args: Array<String>)  
{ 
    //declaring a data class  
    data class man(val name: String, val age: Int) 
    { 
        //property declared in class body 
        var height: Int = 0; 
    } 
       
    val man1 = man("manish",18) 
   
    //copying details of man1 with change in name of man 
    val man2 = man1.copy(name="rahul") 
   
    //copying all details of man1 to man3 
    val man3 = man1.copy(); 
   
    //declaring heights of individual men 
    man1.height=100
    man2.height=90
    man3.height=110
   
    //man1 & man3 have different class body values, 
    //but same parameter values 
   
    //printing info all 3 men 
    println("${man1} has ${man1.height} cm height") 
    println("${man2} has ${man2.height} cm height") 
    println("${man3} has ${man3.height} cm height") 
   
} 
```

### hashCode() and equals()
* hashCode() function returns a hash code value for the object.
* equals() method return true if two objects have same contents and it works similar to “==”, but works different for Float and Double values.

#### Declaration of hashCode() :
```
open fun hashCode(): Int
```
#### Properties of hashCode()

Two hash codes declared two times on same object will be equal.
If two objects are equal according to equals() method, then the hash codes
returned will also be same
```
fun main(args: Array<String>)  
{ 
    //declaring a data class  
    data class man(val name: String, val age: Int) 
       
    val man1 = man("manish",18) 
    val man2 = man1.copy(name="rahul") 
    val man3 = man1.copy(); 
   
    val hash1=man1.hashCode(); 
    val hash2=man2.hashCode(); 
    val hash3=man3.hashCode(); 
   
    println(hash1) 
    println(hash2) 
    println(hash3) 
   
    //checking equality of  these hash codes 
    println("hash1 == hash 2 ${hash1.equals(hash2)}") 
    println("hash2 == hash 3 ${hash2.equals(hash3)}") 
    println("hash1 == hash 3 ${hash1.equals(hash3)}") 
 }
 ```
## Kotlin Abstract class

In Kotlin, abstract class is declared using the abstract keyword in front of class. An abstract class can not instantiated means we can not create object for the abstract class.

### Abstract class declaration:
```
abstract class className {
    .........
} 
```
#### Points to remember:

1. We can’t create an object for abstract class.
2. All the variables (properties) and member functions of an abstract class are by default non-abstract. So, if we want to override these members in the child class then we need to use open keyword.
3. If we declare a member function as abstract then we does not need to annotate with open keyword because these are open by default.
4. An abstract member function doesn’t have a body, and it must be implemented in the derived class.

An abstract class can contain both **abstract** and **non-abstract** members as shown below:
```
abstract class className(val x: String) {   // Non-Abstract Property
         
    abstract var y: Int      // Abstract Property

    abstract fun method1()   // Abstract Methods

    fun method2() {          // Non-Abstract Method
        println("Non abstract function")
    }
}
```
### Multiple derived classes –
An abstract member of an abstract class can be overridden in all the derived classes.

Kotlin **Class Properties and Custom Accessors**

The basic and most important idea of a class is the **Encapsulation**. It is a property to encapsulate code and data, into a single entity. In Java, the data are stored in the fields and these are mostly private.
So, accessor methods – a getter and a setter are provided to let the clients of the given class access the data. For sending notifications about the change or validating the passed value, additional logic is also present in the setter.

Property –
It is the combination of accessories and the fields in case of Java. In case of Kotlin, properties are meant to be a first-class language feature. These features replace fields and accessor methods. A property in a class is declared the same as declaring a variable with val and var keywords. A property declared as var is mutable and thus, can be changed

Defining a class :

```
class Abc( 
    val name: String,  
    val ispassed : Boolean 
) 
```
1. **Readable property** – generates a field and a trivial getter
2. **Writable property** – a getter, a setter and a field

Basically what happens is that the declaration of the property declares the related accessors (both setter and getter for writable and getter for readable property). A field stores the value.

## Customer Accessors
Custom implementation of property accessor.

```
class Rectangle(val height: Int, val width: Int) 
{  
    val isSquare: Boolean 
        get() { 
            return height == width 
        } 
} 
   
fun main(args: Array<String>) { 
   
    val rectangle = Rectangle(41, 43) 
    println(rectangle.isSquare)      
} 
```

## Kotlin constructor

A constructor is a special member function that is invoked when an object of the class is created primarily to initialize variables or properties. A class needs to have a constructor and if we do not declare a constructor, then the compiler generates a default constructor.

### Kotlin has two types of constructors –

* Primary Constructor
* Secondary Constructor

A class in Kotlin can have at most one primary constructor, and one or more secondary constructors. The primary constructor initializes the class, while the secondary constructor is used to initialize the class and introduce some extra logic.

### Primary Constructor –
The primary constructor is initialized in the class header, goes after the class name, using the constructor keyword. The parameters are optional in the primary constructor.
```
class Add constructor(val a: Int, val b: Int) {
     // code
}
```
The constructor keyword can be omitted if there is no annotations or access modifiers specified.
```
class Add(val a: Int, val b: Int) {
     // code
}
```

### Kotlin program of primary constructor –
```
//main function 
fun main(args: Array<String>) 
{ 
    val add = Add(5, 6) 
    println("The Sum of numbers 5 and 6 is: ${add.c}") 
} 
//primary constructor 
class Add constructor(a: Int,b:Int) 
{ 
    var c = a+b; 
} 
```

### Secondary Constructor –
As mentioned above, Kotlin may have one or more secondary constructors. Secondary constructors allow initialization of variables and allow to provide some logic to the class as well. They are prefixed with the constructor keyword.

Kotlin program of implementing secondary constructor-

```
//main function 
fun main(args: Array<String>) 
{ 
    Add(5, 6) 
} 
//class with one secondary constructor 
class Add 
{ 
    constructor(a: Int, b:Int) 
    { 
        var c = a + b 
        println("The sum of numbers 5 and 6 is: ${c}") 
    } 
} 
```
