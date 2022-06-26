# Functions

Default parameters

Named arguments

[Generic Functions](https://kotlinlang.org/docs/functions.html#generic-functions) 

```kotlin
fun <T> singletonList(item: T): List<T> { /*...*/ }
```

Single-expression functions

```kotlin
fun double(x: Int): Int = x * 2
```

```kotlin
tailrec fun findFixPoint(x: Double = 1.0): Double = if (Math.abs(x - Math.cos(x)) < eps) x else findFixPoint(Math.cos(x))
```