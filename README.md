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

### What else to print

    print(10, 30, "ABC", true)
    print("1 + 2 = \(1 + 2)")
