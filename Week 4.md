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
  
