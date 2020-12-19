# Kotlin 
## Introduction
Kotlin is a cross-platform , statically typed, general-purpose programming language with type inference. Kotlin is designed to interoperate fully with Java, and the JVM version of Kotlin's standard library depends on the Java Class Library, but type inference allows its syntax to be more concise.
Kotlin mainly targets the JVM, but also compiles to JavaScript (for e.g. frontend web applications using React) or native code (via LLVM), e.g. for native iOS apps sharing business logic with Android apps.
Language development costs are borne by JetBrains, while the Kotlin Foundation protects the Kotlin trademark.
## History
In July 2011, JetBrains unveiled Project Kotlin, a new language for the JVM, which had been under development for a year. JetBrains lead Dmitry Jemerov said that most languages did not have the features they were looking for, with the exception of Scala. However, he cited the slow compilation time of Scala as a deficiency. One of the stated goals of Kotlin is to compile as quickly as Java.
In February 2012, JetBrains open sourced the project under the Apache 2 license.

The name comes from Kotlin Island, near St. Petersburg. Andrey Breslav mentioned that the team decided to name it after an island just like Java was named after the Indonesian island of Java (though the programming language Java was perhaps named after the coffee).

JetBrains hopes that the new language will drive IntelliJ IDEA sales. Kotlin v1.0 was released on 15 February 2016. This is considered to be the first officially stable release and JetBrains has committed to long-term backwards compatibility starting with this version.

At Google I/O 2017, Google announced first-class support for Kotlin on Android. Kotlin v1.2 was released on 28 November 2017. Sharing code between JVM and JavaScript platforms feature was newly added to this release (as of version 1.4 multiplatform programming is an alpha feature[18] upgraded from "experimental"). A full-stack demo has been made with the new Kotlin/JS Gradle Plugin.

Kotlin v1.3 was released on 29 October 2018, bringing coroutines for asynchronous programming. On 7 May 2019, Google announced that the Kotlin programming language is now its preferred language for Android app developers.

Kotlin v1.4 was released in August 2020, with e.g. some slight changes to the support for Apple's platforms, i.e. to the Objective-C/Swift interop.

## Inside Kotlin
In Kotlin, everything is an object in the sense that we can call member functions and properties on any variable. Some of the types can have a special internal representation - for example, numbers, characters and booleans can be represented as primitive values at runtime - but to the user they look like ordinary classes. 
In this section we describe the basic types used in Kotlin: numbers, characters, booleans, arrays, and strings.

1. Numbers:

Kotlin provides a set of built-in types that represent numbers.
For integer numbers, there are four types with different sizes and, hence, value ranges.

* Byte	
  * 8 bit size.
  * -128 Minimum value.
  * 127 Maximum value.
* Short	
  * 16 bit size.
  * -32768 Minimum value.
  * 32767 Maximum value.
* Int	
  * 32 bit size.
  * -2,147,483,648 minimum value.
  * 2,147,483,647 maximum value.
* Long	
  * 64 bit size.
  * -9,223,372,036,854,775,808 minimum value.
  * 9,223,372,036,854,775,807 maximum value.
2. Characters:
  
Characters are represented by the type Char. They can not be treated directly as numbers.
> fun check(c: Char) {
>
>    if (c == 1) { // ERROR: incompatible types
>
>        // ...
>
>    }
>
> }

Character literals go in single quotes: '1'. Special characters can be escaped using a backslash.
The following escape sequences are supported: \t, \b, \n, \r, \', \", \\ and \$. 
To encode any other character, use the Unicode escape sequence syntax: '\uFF00'.

3. Booleans:

The type Boolean represents booleans, and has two values: true and false.

Booleans are boxed if a nullable reference is needed.

Built-in operations on booleans include:

- ||- Lazy disjunction.
- &&- lazy conjunction.
- !-negation.

4. Arrays:

Arrays in Kotlin are represented by the Array class, that has get and set functions (that turn into [] by operator overloading conventions), and size property, along with a few other useful member functions:

>class Array<T> private constructor() {
>
>   val size: Int
>
>   operator fun get(index: Int): T
>
>   operator fun set(index: Int, value: T): Unit
>
>   operator fun iterator(): Iterator<T>
>
>    / / ...
>
>}
To create an array, we can use a library function arrayOf() and pass the item values to it, so that arrayOf(1, 2, 3) creates an array [1, 2, 3]. Alternatively, the arrayOfNulls() library function can be used to create an array of a given size filled with null elements.
Another option is to use the Array constructor that takes the array size and the function that can return the initial value of each array element given its index:

- Primitive type arrays
    - Kotlin also has specialized classes to represent arrays of primitive types without boxing overhead: ByteArray, ShortArray, IntArray and so on. These classes have no inheritance relation to the Array class, but they have the same set of methods and properties.
    Each of them also has a corresponding factory function:
>val x: IntArray = intArrayOf(1, 2, 3)
>
>x[0] = x[1] + x[2]


[For more basics of Kotlin](https://kotlinlang.org/docs/reference/basic-types.html)
