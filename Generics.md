[[Type Theory]]


[Liskov Substitution Principle](https://en.wikipedia.org/wiki/Liskov_substitution_principle): a variable of a given type may be assigned a value of any subtype
of that type, and a method with a parameter of a given type may be invoked with an
argument of any subtype of that type. 

Generic Type: A generic type is a generic class or interface that is parameterized over types.

```java
@FunctionalInterface  
public interface Function<T, R> {
```

[Generic method](https://docs.oracle.com/javase/tutorial/java/generics/methods.html):  a type parameter living within the scope of that method. 
  
```java
public static <T> T methodName(T t) {}

boolean same = Util.<Integer, String>compare(p1, p2); //explicit type args

public static <T> void sort(List<T> list, Comparator<? super T> c) {list.sort(c);}

<R> Stream<R> map(Function<? super T, ? extends R> mapper);

```


Type inference is a Java compiler's ability to look at each method invocation and corresponding declaration to determine the type argument (or arguments) that make the invocation applicable. Infer type is Serializable:

```java
static <T> T pick(T a1, T a2) { return a2; }

Serializable s = pick("d", new ArrayList<String>());
```

Target type of an expression is the data type that the Java compiler expects depending on where the expression appears.

  
[Type Parameter and Type Argument Terminology](https://blog.kotlin-academy.com/programmer-dictionary-parameter-vs-argument-type-parameter-vs-type-argument-b965d2cc6929): Many developers use the terms "type parameter" and "type argument" interchangeably, but these terms are not the same. T in Foo<T> is a type parameter and String in Foo<String> f is a type argument.  
**_Type parameter_** is blueprint or placeholder for a type declared in generic. **_Type argument_** is actual type used to parametrize generic.

  

Raw type: is the name of a generic class or interface without any type arguments.
  

[Type Erasure](https://docs.oracle.com/javase/tutorial/java/generics/erasure.html) type information is not available to the JVM at runtime, only compile time. During the type erasure process, the Java compiler erases all type parameters and replaces each with its first bound if the type parameter is bounded, or Object if the type parameter is unbounded.

  

[Reified type parameters](https://docs.oracle.com/javase/tutorial/java/generics/nonReifiableVarargsType.html): allow you to refer at runtime to the specific types used as type arguments in an inline function call. (For normal classes or functions, this isn’t possible, because type arguments are erased at runtime.

  

[Restrictions on Generics](https://docs.oracle.com/javase/tutorial/java/generics/restrictions.html)

  

PECS

? extends for covariance PE

? super for [contravariance](https://www.youtube.com/watch?v=tlAGSScIu_w) CS

  

Return type in java is [covariant](https://www.baeldung.com/java-covariant-return-type)

  

At RT List<String> and List<Integer> are the same : List

  

At CT

1.  Replace generic types with objects
    
2.  Replace bounded types (More on these in a later question) with the first bound class
    
3.  Insert the equivalent of casts when retrieving generic objects.
    

[Producer extends, consumer supplies](http://stackoverflow.com/questions/2723397/what-is-pecs-producer-extends-consumer-super)

  
  

[Wildcard Usage](https://docs.oracle.com/javase/tutorial/java/generics/wildcardGuidelines.html)

  

-   E - Element (used extensively by the Java Collections Framework)
    
-   K - Key
    
-   N - Number
    
-   T - Type
    
-   V - Value
    
-   S,U,V etc. - 2nd, 3rd, 4th types
    

  

Questions

[1](https://javarevisited.blogspot.com/2012/06/10-interview-questions-on-java-generics.html)

[2](https://programtalk.com/java/java-generics-interview-questions/)