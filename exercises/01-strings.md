# Exercise 3 — Concatenation Predictions

Predict every result **before** running anything. Be exact — include spaces.

Assume: `int a = 5;  int b = 3;  String s = "Score";  char c = 'A';`

| # | Expression | Predicted | Actual | Right? |
|---|---|---|---|---|
| 1 | `s + a` | Score5 | Score5 | Yes |
| 2 | `s + a + b` | Score53 | Score53 | Yes |
| 3 | `s + (a + b)` | Score8 | Score8 | Yes |
| 4 | `a + b + s` | 8Score | 8Score | Yes |
| 5 | `a + (b + s)` | 53Score| 53Score | Yes |
| 6 | `"" + a +  b` | ""53 | 53 | Wrong because it doesnt print quotes |
| 7 | `c + 1` | A1 | 66 | Wrong because all characters are equal to 65 |
| 8 | `"" + c + 1` | ""A1 | A1 | Wrong because quotes dont print |
| 9 | `(char)(c + 1)` | A1 | B | Because we are casting char so our answer has to be a character |
| 10 | `s + c` | ScoreA| ScoreA| Yes |

---

## Follow-up

**1. Compare #2 and #4. Same three values, opposite order, and the results are structurally different. Explain the rule.**

They are in diffrent orders. If there are () it would add but since in the firstg there isnt it combines to 53. But for 4 it doesnt need () because its in the beginning of the equation.

**2. Why does #7 give `66` instead of `A1`?**

Because character A give a value of 65 so 65 plus one is 66. The character gives a value when its an int connected to a char.

**3. Why does #8 give `A1` when #7 gives `66`? What did the empty string change?**

Since number 8 has string also it prints the letter. Its not int and 

**4. Write a single line that prints exactly `The total of 5 and 3 is 8` using the variables `a` and `b`.**

```java
int a = 5;
int b = 3;
System.out.println("The total of " + a + " and " + b + " is " + (a+b));
```

---

## Immutability check

Run this:
```java
String word = "hello";
word.toUpperCase();
System.out.println(word);

word = word.toUpperCase();
System.out.println(word);
```

**1. What did each line print?**

First line printed hello second line printed HELLO.

**2. In your own words: what does it mean that Strings are immutable?**

It means that you can change the string. 

**3. Why is it easy to write `word.toUpperCase();` and think you've changed something? What kind of error is this — syntax, runtime, or logic?**

This is a logic error. Since it wont say error but its the wrong answer. We would think that would make everything uppercase but we accually need to do it in the println. 
