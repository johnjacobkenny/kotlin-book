# Picking random items

Generating random number from a range or picking a random element from a range is a common requirement. Here we can see how to use Kotlin ranges to pick random items.

## Random number

![](../.gitbook/assets/image%20%285%29.png)

Here the 1..3 range operator generates the range 1 to 3 including 3. Then when we call random\(\) on that, it gives us a random element from that.

```kotlin
(1..4).random()
```

## Random character

![](../.gitbook/assets/image%20%283%29.png)

Here the 'a'..'e' range operator generates the range a to e including e. Then when we call random\(\) on that, it gives us a random element from that.

```kotlin
('a'..'e').random()
```

## Pick random item from list

![](../.gitbook/assets/image%20%284%29.png)

```kotlin
listof("abc", "def", "ghi").random()
```

## References

{% embed url="https://kotlinlang.org/docs/ranges.html\#progression" %}



