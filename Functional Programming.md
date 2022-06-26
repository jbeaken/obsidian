A **higher order function** is a function that takes a function as an argument, or returns a function.

```kotlin
fun sendData(data: Data, callback: () -> Unit) {  
    thread {  
        api.sendData(data)  
        callback()  
    }  
}
```

Here is an example of higher order function that returns a function:

```kotlin
fun makeLogger(for: Any) = fun(e: Error) { 
    Log.e(for::class.simpleName, e.message ?: "Error", e) 
}// Usage in MainActivity
val logger = makeLogger(this)
val error = Error("Simple error")
logger(error) // Logs: MainActivity: Simple error ...
```

Analogically we use term **first order functions** to reference function that doesn’t take a function as an argument or return a function as output.

References