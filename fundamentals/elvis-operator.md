# Elvis operator

`NullPointerException` was an issue in Java. There was less visibility into whether an object could be null, and this was a runtime exception. 

## Nullable types in Kotlin

Kotlin provides first class support as language features to see which objects can be null and which aren't. In the example below, we can see that an object which is not marked as nullable cannot be assigned a null value. The compiler will generate an error at compile time and refuse to compile.

```kotlin
var name: String = "abc" // this is non null
name = null // this will not work since String type does not accept null
```

```kotlin
var name: String? = "abc" // this is non null
name = null // this will work since String? type accepts null
```

This is a very useful feature because we can know which variables can be null, and which variables definitely are not null.

## Elvis Operator

In order to work with the variables that can be null, Kotlin provides many constructs, one of which is the Elvis operator.

So the Elvis operator is defined in wikipedia as,

> In certain computer programming languages, the Elvis operator ?: is a binary operator that returns its first operand if that operand is true, and otherwise evaluates and returns its second operand. It is a variant of the ternary conditional operator, ? :, found in those languages \(and many others\): the Elvis operator is the ternary operator with its second operand omitted.

### Syntax

Here is the rough syntax for the operator,

```kotlin
variable ?: "any value or expression if variable is null"
```

So what this is saying is that Kotlin will first check if the variable is not null. If so then that same variable is the result of that expression. But if it is null, then the second part \(in this example a string\) is what is the result of that expression. And this can be assigned to any variable too.

### Examples

Here is a diagram showing how it works.

![](../.gitbook/assets/elvis-operator.png)

And here is the sample code for it.

```kotlin
//     when b is non null
       var b: String = "Kenny"
       var c: String = "Proful"
       var a = b ?: c
       println(a)
    
//     when b is null
       var b: String? = null
       var c: String = "Proful"
       var a = b ?: c
       println(a)
    
//     when b and c are null
       var b: String? = null
       var c: String? = null
       var a = b ?: c
       println(a)
    
//     example with if condition
       var b: String = "Kenny"
       var c: String = "Proful"
       var a = if (b != null) b else c
       println(a)
```

## Why is it called Elvis operator?

This operator when rotated looks like the famous singer Elvis Presley's hairstyle.

![](../.gitbook/assets/elvis-operator-hair.png)

## References

{% embed url="https://kotlinlang.org/docs/null-safety.html\#elvis-operator" %}

{% embed url="https://stackoverflow.com/questions/48253107/what-does-do-in-kotlin-elvis-operator" %}

{% embed url="https://excalidraw.com/\#json=4827141933891584,Ldn0fH\_ZGXN7N1rR3xXu4g" %}





