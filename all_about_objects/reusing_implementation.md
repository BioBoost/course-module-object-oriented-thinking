## Reusing Implementation

Once a class has been created and hopefully tested it should ideally represent a useful unit of code.  In this case it begs to be reused and not go to waste. It also turns out that code reuse is one of the main advantages of object oriented programming.

> #### Warning::Reuse and DRY
>
> Code reuse is not, as some understand it to be (students in particular), the ability to be copy pasted from one part inside your program to another! This is actually *code duplication* and is considered bad practice. The DRYness (DRY - Don't Repeat Yourself) of once code is one of the indicators of the maintainability of that code.

Multiple ways exist to reuse a class:

* **Association**: Just use the objects of a class.
* **Composition** and **Aggregation**: Build classes that consist of other objects.
* **Inheritance**: Extend an existing class by inheriting from a base class.

Do note that the this relationship depends on the actual definition of the Student and Teacher classes. In other words, it can differ from application to application.

### Association

The simplest way to reuse a class is by creating objects from it and using those objects. In other words an object of one class may use services/methods provided by an object of another class. This kind of relationship is termed as an **association**.

An association represents a relationship between two or more objects where all objects have their own lifecycle and there is no owner. The name of an association specifies the nature of relationship between objects. This is represented in UML by a solid line.

> #### Info::Life Cycle
>
> The life cycle of an object is the time between an object's creation and its destruction. Rules for object lifetime vary significantly between languages, in some cases between implementations of a given language, and lifetime of a particular object may vary from one run of the program to another.

Let's take an example of relationship between Teacher and Student. Multiple students can associate with a single teacher and a single student can associate with multiple teachers. But there is no ownership between the objects and both have their own lifecycle. Both can be created and deleted independently.

![Teacher has an Association with Student](img/association.png)

Another example could be an Employee who uses instances of the class Company Computer. While the computer objects are owned by the employee's company, he can make use of them.

![Employee uses a Company Computer](img/employee_computer.png)

### Composition

It's natural to think of **objects as collections of other objects**. Think about a television which contains a tuner, a screen, a power supply, an embedded system, ... We say that a television object is **composed** of these other objects. Luckily this same concept is available to us in an object oriented programming language. We can also create objects by bundling other objects. This has the big advantage that we can use objects from classes that someone else made or are part of the language libraries. This saves us a lot of time and effort. This sort of code reuse is one of the major advantages of object oriented languages.

In a composition relationship child objects do not have their own lifecycle. If a parent object is destroyed, all its child objects will also be destroyed. This represents a "death-relationship". In UML this is represented by a solid diamond followed by a line.

Let's take an example of relationship between a House and a Room. House can contain multiple rooms, but there is no independent life of Room and a Room cannot belong to two different houses. If we destroy the house, the rooms will automatically be destroyed too.

![Composition relationship between House and Room](img/composition.png)

So composition implies a relationship where the child cannot exist independent of the parent.

Take for example an object of class Person that is composed of other objects such as a head, two feet, a heart, ... If the person is destroyed his/her limbs and organs also die. This of course does not take into account organ transplantation.

![Person as a Composition](img/person_composition.png)

### Aggregation

Aggregation implies a relationship where the child can exist independently of the parent.

**Aggregation** is a specialized form of association where all object have their own lifecycle but there is ownership. This represents "whole-part or a-part-of" relationship between the aggregate (whole) and a component part. In UML this is represented by a hollow diamond followed by a line.

Let's take an example of a relationship between Department and Teacher. A Teacher may belong to multiple departments. Hence Teacher is a part of a Department. But if we delete a Department object, no Teacher objects will be destroyed.

![Aggregation relationship between Department and Teacher](img/aggregation.png)

Take for example a Car. If the parts of the car can be reused after the car is destroyed, than we can create a Car as an aggregation of Wheels, an Engine, a Radio, ...

![Car as an Aggregation](img/car_aggregation.png)

### Summarized

While a clear distinction is made here between aggregation and composition, it is not always so clear in practice. Often one does speak of composition even if he/she were to mean aggregation. As a result this course may also use the word composition where aggregation is meant. Of course in cases where a clear distinction is needed, the correct term will be used.

To sum it up, association is a very generic term used to represent when one class uses the functionalities provided by another class. It's a composition relationship if one parent class object owns another child class object and that child class object cannot meaningfully exist without the parent class object. If it can then it is called aggregation.
