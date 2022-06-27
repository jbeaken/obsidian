write out the map function from java.util.Collections\<T>

```java
public <R> Stream<R> map(Function<? super T, ? extends R> mapper)
```


```java
public <R> void sort(Collection<R> list, Comparator<? super R comparator);

public static <T> void sort(List<T> list, Comparator<? super T> c) {list.sort(c);}
```