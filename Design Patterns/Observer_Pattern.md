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















