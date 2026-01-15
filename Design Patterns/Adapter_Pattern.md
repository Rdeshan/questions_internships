Adapter Design Pattern — Full Definition

Definition (Formal):
The Adapter Pattern is a structural design pattern that allows objects with incompatible interfaces to work together. It acts as a bridge 
between two interfaces by converting the interface of a class into another interface that a client expects.
Purpose: Enable integration of existing classes into a system without modifying their source code.

Category: Structural pattern (it deals with how classes and objects are composed to form larger structures).

Key Points

Problem it solves:

You have a class A with a certain interface.

You want to use it in a system that expects interface B.

Direct use is impossible because A’s methods do not match B.

Solution:

Create an Adapter class that implements interface B and internally uses an instance of A to perform the actual work.

The Adapter translates calls from the client to the adaptee.

Participants:

Target: The interface expected by the client.

Client: The class that uses the Target interface.

Adaptee: The existing class with a different interface.

Adapter: A class that implements the Target interface and makes the Adaptee compatible with the Client.

Analogy (Real Life Example)

Think of an electrical plug adapter.

Your phone charger has a US plug, but your wall socket is EU type.

The adapter converts the plug type so the charger works with the socket.

Here,

Charger → Adaptee

Socket → Target

Plug Adapter → Adapter

When to Use

You want to reuse existing classes that don’t match the system interface.

You want to integrate third-party code without modifying it.

You need to convert interfaces to make them compatible.

Types of Adapter

Class Adapter – Uses inheritance to adapt one interface to another.

Object Adapter – Uses composition; holds an instance of Adaptee and delegates calls to it (more flexible, preferred in most cases).
