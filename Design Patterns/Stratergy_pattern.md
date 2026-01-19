1. What is the Strategy Design Pattern? (Simple idea)

The Strategy Pattern is a behavioral design pattern that allows you to define multiple algorithms (strategies), put each one in a separate class, and switch between them at runtime without changing the main (client) code.

👉 In simple words:

Strategy Pattern lets you choose different ways of doing something while the program is running.

2. Why do we need the Strategy Pattern?

Imagine this situation:

You have a program that does payment processing
Sometimes you pay by Credit Card
Sometimes by PayPal
Sometimes by Cash

❌ If you write all logic using if-else or switch statements:

Code becomes messy
Hard to add new payment methods
Violates clean code principles

✅ Strategy Pattern solves this by:

Separating each algorithm
Making code flexible
Making it easy to extend

3. Formal Definition (Exam / Textbook Style)

The Strategy Pattern defines a family of algorithms, encapsulates each one, and makes them interchangeable. It allows the algorithm to vary independently from the clients that use it.

4. Key Concepts of Strategy Pattern

There are three main parts:

1️⃣ Strategy (Interface)

Declares a common interface for all algorithms
Example: PaymentStrategy

2️⃣ Concrete Strategy

Implements the strategy interface
Each class contains one specific algorithm
Example: CreditCardPayment, PayPalPayment

3️⃣ Context

Uses a Strategy object
Does not know which algorithm is used
Example: PaymentProcessor

5. How Strategy Pattern Works (Step by Step)

Create a strategy interface
Create multiple classes implementing that interface
Create a context class
Pass the desired strategy to the context
The context executes the algorithm via the interface

6. Real-World Example (Easy to Understand)
Problem

You are traveling and want to go somewhere:

By Bus
By Train
By Car

The destination is same, but strategy (travel method) changes.

👉 That is Strategy Pattern.

7. UML Structure (Conceptual)

```
Client
   |
Context --------> Strategy (interface)
                     |
          -------------------------
          |           |           |
   ConcreteStrategyA  B   ConcreteStrategyC

```

8. Example in Plain English

Strategy → “How should I do this task?”

Concrete Strategy → “This is one specific way”

Context → “I don’t care how, just do it”

9. Advantages of Strategy Pattern

✅ Removes large if-else or switch blocks
✅ Follows Open–Closed Principle
✅ Easy to add new strategies
✅ Cleaner and more maintainable code
✅ Algorithms are reusable

10. Disadvantages of Strategy Pattern

❌ Increases number of classes
❌ Client must know which strategy to use
❌ Can be overkill for simple programs

11. When to Use Strategy Pattern

Use Strategy Pattern when:

You have multiple ways to perform an action
You want to change behavior at runtime
You want to avoid conditional logic
You want cleaner, extensible code
