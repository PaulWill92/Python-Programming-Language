# Python intermediate course

[David Beazley](https://learning.oreilly.com/videos/python-programming-language/9780134217314/9780134217314-PYMC_01_02/)

## Course Outline

Lesson 1: Working Environment

Lesson 1 introduces the basics of working in the Python programming environment. This includes starting and stopping the interpreter, using the interactive console, editing and running programs, and turning simple programs into useful scripts. Getting help and some basic debugging tips are also described.

Lesson 2: Program Structure and Execution Model

Lesson 2 covers Python’s execution model and describes the statements related to variables, expressions, and simple control flow. It also covers using Python to perform simple mathematical calculations, making formatted output, and writing to a file.

Lesson 3: Text Processing and Files

To do almost anything useful, you need to be able to read data into your program. Lesson 3 addresses the problem of reading data from a file, basic techniques for manipulating text strings, converting input data, and performing calculations. It also introduces the csv module for reading data from CSV files.

Lesson 4: Functions and Error Handling

As you write larger programs, you will want to get organized. The primary way of doing this in Python is to write functions. And if you write functions, you will want them to play nicely with others. Lesson 4 addresses the problem of writing function definitions, handling exceptions, and coding practices that will help you when you start to write larger programs.

Lesson 5: Data Structures and Data Manipulation

One of the most critical Python skills to develop is being able to effectively use lists, tuples, sets, and dictionaries. Lesson 5 includes how to read a file into a useful data structure. It then explores different ways of performing calculations on the data, including data reductions, filtering, joining, and sorting. Particular attention is given to list, set, and dict comprehensions a feature that greatly simplifies a wide variety of data processing tasks.

Lesson 6: Library Functions and Import

As you write larger Python programs, you will want to write library functions and split your code across multiple files. To do this, you need to start working with modules and packages. Lesson 6 delves into creating and using modules. It starts with how to use the import statement and some of its gotchas. Next it covers how to create a general purpose CSV parsing function and apply it to some of our earlier code. The lesson concludes with a discussion of organizing larger code bases into packages.

Lesson 7: Classes and Objects

Object-oriented programming is a fundamental part of the Python language. You see this whenever you use its built-in types and execute methods on the resulting instances. If you want to make your own objects, you can do so using the class statement. A class is often a convenient way to define a data structure and to attach methods that carry out operations on the data. Lesson 7 covers the basics of defining a new object, creating instances, and manipulating objects. It then helps you see how the dynamic nature of Python enables you to write highly generic functions. The Lesson concludes with a special topic on how to write classes that need to have more than one initializer method.

Lesson 8: Inheritance

One of the most challenging problems in writing larger programs is that of code reuse and extensibility. A common tool used to address this problem is inheritance. Lesson 8 addresses using inheritance to make a program extensible as well as some of the tricky practical concerns that might arise as a result. Some advanced inheritance concepts, such as multiple inheritance with mixin classes and abstract base classes, are also introduced. The lesson concludes by discussing a few important design considerations to take into account if you’re going to use inheritance.

Lesson 9: Python Magic Methods (a.k.a., Speaking Python)

When defining new objects, it is usually beneficial to make your objects play nicely with other parts of Python. This is typically done by adding special or "magic" methods to your class. Lesson 9 demonstrates some of the common customizations that are made to objects to simplify debugging, create containers, and manage resources. Although this section doesn’t cover every possible customization that can be carried out, it gives you a taste of what’s possible and a foundation for more exploration.

Lesson 10: Encapsulation (Owning the Dot)

Major issues that arise in larger programs are how to encapsulate internal implementation details and how to have more control over the ways in which developers interact with objects. Lesson 10 dives into some of the low-level details that make the Python object system tick. It then turns to techniques for taking control over attribute access and custom-tailoring the environment to address issues such as data validation, type checking, and more. Topics include defining private attributes, properties, descriptors, and redefining magic methods for attribute access.

Lesson 11: Higher Order Functions and Closures

Functions are the basic organizational unit of all Python programs regardless of whether or not they serve as a stand-alone function or the method of a class. Lesson 11 introduces some important functional programming concepts, including the idea of functions as first class objects, passing functions as data, and creating functions as results. Particular emphasis is placed on closures as a tool for generating and simplifying code.

Lesson 12: Metaprogramming and Decorators

One of the most difficult problems in developing larger programs is dealing with highly repetitive code. For example, as a general rule you want to avoid situations where you’re cutting and pasting common code fragments between functions or across files. Restructuring the design of your program might help solve such problems. However, another common technique is to encapsulate common code-oriented tasks into a decorator. Lesson 12 covers how to write decorators for processing both function and class definitions.

Lesson 13: Metaclasses

One of the problems faced by the creators of large applications and frameworks is exercising control over the greater programming environment. Code is often organized using classes, but sometimes there is much more to it than simply making class definitions. For example, classes might need to register their existence with some other part of a framework. Or perhaps the definition of a class is too verbose and needs to be simplified in some way. Or perhaps some other aspect of classes needs to be managed. An advanced technique for addressing these problems is to use a metaclass. Lesson 13 introduces the metaclass concept and some practical applications are shown.

Lesson 14: Iterators and Generators

One of Python’s most useful features is the for-statement, which is used to iterate over data. As you may have noticed, the for-statement works with a wide variety of objects such as lists, dicts, sets, and files. It’s also used in a variety of related features, such as list comprehensions. One of the most powerful features of iteration is that it can be easily customized. Lesson 14 starts with the iteration protocol and how to customize it using generator functions. It also covers how to apply iteration to data processing pipelines a particularly powerful technique for working with data and problems involving workflows.

Lesson 15: Coroutines

Starting in Python 3.5, a special kind of function known as a "coroutine" could be defined using special async/await syntax. On the surface, coroutines look a lot like normal Python functions. However, under the covers they run under the supervision of a manager that coordinates their execution. Lesson 15 introduces coroutines and shows how they can be used to implement a simple network service that can handle thousands of concurrent client connections. It concludes by peeling back some of the covers to see how coroutines actually work and to explore their relationship to generators.
