# Repeat operator

inline fun repeat\(times: Int, action: \(Int\) -&gt; Unit\)





// greets three times repeat\(3\) { println\("Hello"\) }

// greets with an index repeat\(3\) { index -&gt; println\("Hello with index $index"\) }

repeat\(0\) { error\("We should not get here!"\) }







{% embed url="https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/repeat.html" %}



