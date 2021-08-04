# Statement vs Expression

Expressions and statements are the basic building block of programs. They help us perform computations and also control the program flow.

Here is the difference in a generic sense.

### Expression

```kotlin
5 * 3
```

Here we can see a simple computation written as an expression. We know that the program will compute and return the value. Let us look at how a statement is.

### Statement

```kotlin
val a = 5
println("Hello world")
```

Here we can see that there are some actions that are performed, or side effects as a result of executing both lines. But there is no return value per se for either of the lines.

### Statement with Expression

```kotlin
val a = 5 * 3
```

Here we can see an expression within the statement, which gets evaluated.

![](../.gitbook/assets/image%20%281%29.png)

### Kotlin Statement vs Expression

So far we saw the differences between statements and expressions as per most object oriented programming languages. Here in Kotlin there is a twist that some language features can act as both statement and as expression depending on the context.

![](../.gitbook/assets/image%20%282%29.png)

```kotlin
val a = 1

if (a < 0) {
  println("$a is negative")
} else {
  println("$a is positive")
}

val result = if (a < 0) {
  "negative"
} else {
  "positive"
}

println("result value is $result")
```

Because of this there is no ternary operator, since the if is an expression and returns a value. In a similar way, we can use the same approach for `when` block and for `try-catch` block. Here are few examples.

```kotlin
val bigger = if(a > b) a else b

val color = when {
    relax -> GREEN
    studyTime -> YELLOW
    else -> BLUE
}

val object = try {
    gson.fromJson(json)
} catch (e: Throwable) {
    null
}
```

### References

{% embed url="https://blog.kotlin-academy.com/kotlin-programmer-dictionary-statement-vs-expression-e6743ba1aaa0" %}

{% embed url="https://kotlinlang.org/docs/control-flow.html\#if-expression" %}

{% embed url="https://kotlinlang.org/docs/control-flow.html\#if-expression" %}



