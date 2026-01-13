factory method is creational design pattern this design pattern provides single place to create objects . Instead of creating objects directly using new keyword . we use factory class or method to create and return required object. because of it hides object creation details inside single factory class

How this works ( Example )

problem :- logistic app handles truck , but it need to add sea transport without changing the core code 
Solution :- 1. define a transport product interface ( e.g - deliver())
            2. create truck and ship products implementing transport 
            3. define logistice creator with an abstract create transport method 
            4. create trucklogistic and sealogistic concrete creators , each implementing createTransport() to return either truck or ship 


``` 1️⃣ Transport (Product Interface)
public interface Transport {
    void deliver();
}
```
```2️⃣ Concrete Products (Truck & Ship)
public class Truck implements Transport {
    @Override
    public void deliver() {
        System.out.println("Delivering cargo by road using a Truck 🚚");
    }
}

public class Ship implements Transport {
    @Override
    public void deliver() {
        System.out.println("Delivering cargo by sea using a Ship 🚢");
    }
}
```
```3️⃣ Logistics (Creator – Abstract Class)
public abstract class Logistics {

    // Factory Method
    public abstract Transport createTransport();

    // Some business logic
    public void planDelivery() {
        Transport transport = createTransport();
        transport.deliver();
    }
}
```
```4️⃣ Concrete Creators (TruckLogistics & SeaLogistics)
public class TruckLogistics extends Logistics {
    @Override
    public Transport createTransport() {
        return new Truck();
    }
}

public class SeaLogistics extends Logistics {
    @Override
    public Transport createTransport() {
        return new Ship();
    }
}
```
```5️⃣ Client Code (Main Class)
public class Main {
    public static void main(String[] args) {

        Logistics logistics1 = new TruckLogistics();
        logistics1.planDelivery();

        Logistics logistics2 = new SeaLogistics();
        logistics2.planDelivery();
    }
}
```
```✅ Output
Delivering cargo by road using a Truck 🚚
Delivering cargo by sea using a Ship 🚢

```

the flow of above scenario happen (**            very important             **)
            Step by step:   1 .TruckLogistics object created
                            2 .planDelivery() called
                            3 .createTransport() → returns Truck
                            4 .deliver() → Truck delivers

Factory method follows Open-close principle ( OCP ) that mean open for extensions , closed for modifications  

**            Factory method does not hide everything it hides only product creation , not creator selection            **







  


