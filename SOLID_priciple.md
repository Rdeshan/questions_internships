--------------------------------------------------------------------------------
The Five Software Rules (SOLID)
1️⃣ S – Single Responsibility Principle (SRP)

👉 A class should have only one reason to change.

Simple idea:
One class = one job.

Example:
❌ A class that handles user data + email sending
✅ One class for user logic, another for email logic
--------------------------------------------------------------------------------

2️⃣ O – Open/Closed Principle (OCP)

👉 Software should be open for extension, but closed for modification.

Simple idea:
You should add new features without changing existing code.

Example:
Use interfaces or inheritance instead of editing old logic every time.

-------------------------------------------------------------------------------------------

3️⃣ L – Liskov Substitution Principle (LSP)

👉 A child class should be able to replace its parent class without breaking the program.

Simple idea:
If Dog is an Animal, anywhere you use Animal, Dog should work correctly.

Bad sign:
If subclass changes expected behavior → violates LSP.

--------------------------------------------------------------------------------------------

4️⃣ I – Interface Segregation Principle (ISP)

👉 Don’t force classes to implement methods they don’t need.

Simple idea:
Many small interfaces ❌ better than one big interface.

Example:
❌ Machine interface with print(), scan(), fax()
✅ Separate interfaces: Printable, Scannable, Faxable
---------------------------------------------------------------------------------------------

5️⃣ D – Dependency Inversion Principle (DIP)

👉 Depend on abstractions, not concrete implementations.

Simple idea:
High-level code should not depend on low-level code directly.

Example:
Use interfaces instead of new MySQLDatabase() directly






