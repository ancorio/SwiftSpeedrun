# Swift Speedrun

**Warning:**  *This is not complete guide to Swift language.*

Hello! If you are already experienced in programming but want to learn a new language this page will be useful for you to get known with the syntax, main features and concepts that you should learn to use the language efficiently.

Practice is the key to learning so don't hesitate to try everything you found useful there by yourself to master that what you've read there.

## Basics
### What is Swift?
Swift is a high-level programming language developed by Apple. It's primarily used for software development for Apple devices but also can be used as a generic purpose language. Before Swift there was `Objective-C`, Swift has several features to have a compatibility with ObjC code, some may be used in ObjC, but there are limitations.

> Knowing on ObjC is important for everyone who develops software for
> Apple products as lot of SDK tools are written on it. As OOP part of
> Swift is using `ARC` - the approach to managing object lifecycle it
> inherited from ObjC. Understanding ARC is one of the first things you
> should do when diving into Swift's OOP.

Apple also introduced term "Protocol Oriented Programming" and a main paradigm of the language. Indeed, understanding the power or protocols and developing protocol-oriented thinking is the key for mastering the language.

### Hello world
Here's how Hello World look like in Swift:

    import Foundation
    print("Hello World!")

`Foundation` the the framework that contains the most basic things you'll need to develop your first program. Here's the link: https://developer.apple.com/documentation/foundation

> An important part of learning the language is learning the SDK, Apple's documentation is pretty convenient, just reading through the list of framework functions and types will give you the understanding of what you are able to do with it. So when during your journey you meet a new framework - go ahead and just look through its docs.

`print` is a function of swift standard library that is user to put things into the console log.

### What else to print?

    print(10, 30, "ABC", true) // Multiple things
    print("1 + 2 = \(1 + 2)") // Put expressions into the String

### Semicolons
Semicolons do exist in Swift but better ever use them, semicolon in the end of the line is not required

    let a = 1; let b = true // You can, but you won't

### Most important basic types

`Bool` - true/false
`Int` - platform-dependent size integer
`Int8/Int16/Int32/Int64` - size-specific integers
`Float/Double` - floating points.
`Float32/Float64` - size-specific floating points.
`String/Date` - guess what.

### Variables definitions
    let a = 5 // constant
    var b = 10 // variable
    a = b // invalid
    b = a // valid
    
When defining a variable you can specify the type or let the compiler to decide:

    let a = 7 // a is Int
    let b: Int64 = 7
    var c = a // c is Int
    var d = b // d is Int64

### Scalar type conversions
    let a = 7 // a is Int
    let b: Int64 = a // invalid
	let c = Int64(a) // That's how you do it


	
### Making a string
    let a = "String 1"
    let b = "More \(a)" // "More String 1"
    let c = String(123)
    let d = String(format: "Float %0.2f", arguments: [12.5])
    let e = a + b
    let f = "X" + String(12) // "X" + 12 will not work
### ! Value types !

> Next thing is really important! If you've never met the concept of value types before you need to get into it for proper understanding of what it going on.

*String is used there and an example of value type, there are lots of other value types there and every day you will create your own*

String in Swift is not a class type, it's a `struct`, something that looks like C's `struct`. The string variable not storing the reference to it but the value itself. This is called **Value type**. When you define a value type variable you define the memory area where the value will be stored. It's like defining the scalar variable, but the structure of it may contain a complex data.

    // Like for Ints
    var i1 = 60
    var i2 = i1
    i2 = 100 // i1 remains 60 because this is an independent variable in separate memory cluster
    // Like for Strings
    var s1 = "60"
    var s2 = s1
    s2 = "100" // s1 remains "60" because this is an independent variable in separate memory cluster

So assigning a value-type variable or forwarding it into function parameter is actually a creation of its identical memory copy. So there is no copy function for value types as "assign" for them means "copy".

There are a lot of explanation of what is Value type over the Internet, please check them out if my explanation doesn't fit for you.

### Why value types?
Lots of things become faster and easier if you don't use classes every time you need to work with more than 1 value at the same time. You don't need copy methods, you don't need to make sure that data that you return as a reference will not be unexpectedly modified somewhere else. Classes lifecycle also consumes a lot of runtime resources when value types are just a chunks of memory that don't need constructors/destructors and a lot of other stuff. Yes, ObjC had struct inherited from C language but they were not integrated with the language itself. In Swift structs, enums and classes share almost all the features that the language have and can be treated similarly in the most cases.

This makes value types more preferable to use everywhere you don't need them to be classes and protocols are helping you to overcome the some limitations that you can face when trying to do so.
