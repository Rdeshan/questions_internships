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


Step 3️⃣ Create ConcreteSubject (YouTube Channel)

```
import java.util.ArrayList;
import java.util.List;

public class YouTubeChannel implements Subject {

    private List<Observer> subscribers = new ArrayList<>();
    private String latestVideo;

    @Override
    public void subscribe(Observer observer) {
        subscribers.add(observer);
    }

    @Override
    public void unsubscribe(Observer observer) {
        subscribers.remove(observer);
    }

    @Override
    public void notifyObservers() {
        for (Observer observer : subscribers) {
            observer.update(latestVideo);
        }
    }

    // Business logic
    public void uploadVideo(String title) {
        this.latestVideo = title;
        notifyObservers();
    }
}
```

📌 Important
Subject does NOT know details of observers
Only knows they have update() method


Step 4️⃣ Create ConcreteObserver (Subscriber)

```
public class Subscriber implements Observer {

    private String name;

    public Subscriber(String name) {
        this.name = name;
    }

    @Override
    public void update(String videoTitle) {
        System.out.println(name + " received notification: New video -> " + videoTitle);
    }
}
```
Step 5️⃣ Test everything (Main class)
```
public class Main {
    public static void main(String[] args) {

        YouTubeChannel channel = new YouTubeChannel();

        Subscriber user1 = new Subscriber("Deshan");
        Subscriber user2 = new Subscriber("Ravindu");

        channel.subscribe(user1);
        channel.subscribe(user2);

        channel.uploadVideo("Observer Pattern Explained!");
    }
}

























