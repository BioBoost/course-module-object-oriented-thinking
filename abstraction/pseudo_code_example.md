## Pseudo Code Example

Let us consider a less abstract example (pun intended).

Take a look at the pseudo code below.

```text
create array[N]
array[0..N-1] = random(time)

i ← 1
while i < N
    j ← i
    while j > 0 and array[j-1] > array[j]
        swap array[j] and array[j-1]
        j ← j - 1
    end while
    i ← i + 1
end while
```

This piece of pseudo code is already an abstraction of an algorithm expressed in a programming language. Can you guess what it does by looking at it for a maximum time of 15 seconds?

Now what if we were to abstract some parts away in functions that we could use inside this algorithm as follows:

```text
create array[N]
initialize_with_random_values(array)
sort(ascending)
```

Now you immediately see that the pseudocode creates an array of random values that then is being sorted in ascending order. That clearness is abstraction at work.
