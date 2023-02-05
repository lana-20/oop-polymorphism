# Polymorhism

__Polymorphism is one of the core concepts of the OOP (Object Oriented Programming).__ Polymorphism is a word composed of two Greek words: _poly_, which means _many_, and _morph_, which means _forms_. Therefore, _polymorphism means many forms_. 

## Compile-Time Polymorphism / Method Overloading
More precisely, in the OOP context, _polymorphism allows an object to behave differently in certain cases_, or, in other words allows an action to be accomplished  in different ways (approaches). _One way to implement polymorphism in Java is via method overloading. This is know as Compile-Time Polymorphism_ because the  compiler can identify at compile time which form of an overloaded method to call (multiple methods with the same name but different arguments). So, depending on which form of the overloaded method is called, the object behaves differently. For example, a class named <code> Triangle </code> can define multiple methods named <code>draw()</code> with different arguments.

Unlike many other popular object-oriented programming languages such as Java, Python doesn’t support compile-time polymorphism or method overloading. If a class or Python script has multiple methods with the same name, the method defined the latest overrides the earlier one.
Python doesn’t use function arguments for method signature, that’s why method overloading is not supported in Python.

Operator Overloading in Python
Python supports operator overloading. This is another type of polymorphism where an operator behaves differently based on the type of the operands.
* + operator adds two numbers and concatenate two strings
* * operator multiplies two numbers and when used with a string and int, repeats the string given int times and concatenate them.
Read More at Operator Overloading in Python.

## Runtime Polymorphism / Method Overriding / Dynamic Dispatch

...

Advantages of Polymorphism
* The scripts and classes written once can be reused and implemented multiple times.
* It helps in reducing the coupling between different functionalities and behavior of objects.

<img width="800" src="https://user-images.githubusercontent.com/70295997/215978161-7ddb3756-0410-45f9-b441-53781bf5ee2a.png">
