[[Type Theory]]
[[Kotlin]]

Any is the super type of classes and intefaces. Same as Object in java but cannot be null

Functions that have side effects can return Unit

Nothing represents value of expression that never completes.

Nullable types form a parallel subtype hierachy. Nullable type is a super type of the non-nullable type#

```kotlin
inteface Store<in T> { fun put(item : T)}
inteface S<out T> {fun take(): T }
```


## References

[Youtube video](https://www.youtube.com/watch?v=juFkdMv4B9s&t=1436s)

