** the definition of observer pattern is when one object changes, and many other objects need to be notified automatically  **
                                          ** this creates one to many relationship**


Simple Example :- 
```
  Imagine this real life situation :- you subscribe to a youtube channel , when the creator uploads a youtube video you
get notification and thousand of people also get notified,
Important point :- the youtuber does not manually notify each people.
subscribers are automatically updated
```
Above scenario is exactly what observer pattern does

```                                              
Subject (YouTube Channel)
   |
   | notify()
   ↓
Observer 1 (User A)
Observer 2 (User B)
Observer 3 (User C)
```
when subject changes all observers notified automatically 


Lets see above example with code based implementation :-

Step 1️⃣ Create Observer interface

```
public interface Observer {
    void update(String message);
}
```
👉 Anyone who wants updates must implement this

Step 2️⃣ Create Subject interface

```
public interface Subject {
    void subscribe(Observer observer);
    void unsubscribe(Observer observer);
    void notifyObservers();
}
```

👉 Subject manages observers


























