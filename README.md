# Class-3 : Python Loops 

---

## Table of Contents

1. Overview
2. Prerequisites
3. What is a loop?
4. `for` loop — explanation + examples
5. `while` loop — explanation + examples
6. `break`, `continue`, and `pass`
7. `else` with loops
8. Nested loops
9. List comprehensions (short intro)
10. Common mistakes & debugging tips
11. Classroom lesson plan (45–60 minutes)
12. Practice exercises (with answers)
13. Teaching tips and assessment

---

## 1. Overview

This README explains Python loops in a step-by-step, beginner-friendly way. Each concept has a short explanation, sample code, expected output, and short exercises you can give to students.

## 2. Prerequisites

Students should know:

* What a variable is
* Basic Python data types: `int`, `str`, `list`
* `print()` function and simple expressions

If not, spend 10–15 minutes quickly reviewing these.

## 3. What is a loop?

A loop repeats a block of code multiple times. We use loops when we want to run the same steps more than once — for example, printing numbers from 1 to 5.

---

## 4. `for` loop — explanation + examples

**Concept:** Use `for` when you want to iterate over items (like a list, string, or range).

**Syntax:**

```python
for item in iterable:
    # do something with item
```

**Example 1 — iterate over a list:**

```python
fruits = ['apple', 'banana', 'mango']
for fruit in fruits:
    print(fruit)
```

**Expected output:**

```
apple
banana
mango
```

**Example 2 — using `range()` to loop numbers:**

```python
for i in range(1, 6):  # from 1 to 5
    print(i)
```

**Expected output:**

```
1
2
3
4
5
```

**Teaching note:** explain `range(start, stop)` where `stop` is exclusive. Show `range(5)` equals `range(0, 5)`.

---

## 5. `while` loop — explanation + examples

**Concept:** Use `while` when you want to repeat until a condition becomes `False`.

**Syntax:**

```python
while condition:
    # do something
```

**Example — count from 1 to 5:**

```python
n = 1
while n <= 5:
    print(n)
    n += 1
```

**Expected output:** same as `for` example above.

**Warning:** If the condition never becomes `False`, the loop runs forever (infinite loop). Teach how to avoid that.

---

## 6. `break`, `continue`, and `pass`

* `break` stops the loop immediately.
* `continue` skips to the next iteration.
* `pass` does nothing — placeholder for future code.

**Example — `break` and `continue`:**

```python
for i in range(1, 6):
    if i == 4:
        break
    print('Before continue:', i)
    if i % 2 == 0:
        continue
    print('After continue (odd):', i)
```

**Explain step-by-step what prints and why.**

---

## 7. `else` with loops

A loop's `else` block runs when the loop finishes normally (no `break`).

**Example:**

```python
for i in range(3):
    print(i)
else:
    print('Loop finished')
```

If loop is stopped by `break`, `else` will not run. This is useful for search patterns.

---

## 8. Nested loops

Loops inside loops. Useful for tables, matrices, or pairs.

**Example — multiplication table (2×2 to 3×3):**

```python
for i in range(2, 4):
    for j in range(2, 4):
        print(i, 'x', j, '=', i * j)
```

**Expected output:**

```
2 x 2 = 4
2 x 3 = 6
3 x 2 = 6
3 x 3 = 9
```

**Teaching tip:** Explain complexity: each outer step runs the whole inner loop.

---

## 9. List comprehensions (short intro)

A compact way to create lists using loops in one line.

**Example — square numbers:**

```python
squares = [x * x for x in range(1, 6)]
print(squares)
```

**Output:** `[1, 4, 9, 16, 25]`

**Note:** Teach after `for` and `while` — it's advanced but useful.

---

## 10. Common mistakes & debugging tips

* Forgetting to update loop variable in `while` → infinite loop.
* Using wrong indentation (Python is indentation-sensitive).
* Expecting `range(1, 5)` to include 5 — it does not.
* Modifying a list while iterating over it — show safe patterns (iterate over a copy `for x in mylist[:]`).

**Debugging tip:** Use `print()` to check values each iteration. Ask: does the condition change as expected?

---

## 11. Classroom lesson plan (45–60 minutes)

**Goal:** Students should understand `for`, `while`, `break`, `continue`, and practice with small tasks.

* 0–5 min: Warm-up and prerequisites check
* 5–15 min: Explain `for` with live coding and examples
* 15–25 min: `range()` practice and short exercises
* 25–35 min: `while` loop and infinite loop example
* 35–45 min: `break`, `continue`, and `else` with examples
* 45–60 min: Exercises, review answers, Q&A

Optional homework: build a simple guessing game using `while` and `break`.

---

## 12. Practice exercises (with answers)

**Exercise 1:** Print even numbers from 2 to 10.

**Student solution:**

```python
for i in range(2, 11, 2):
    print(i)
```

**Exercise 2:** Sum numbers from 1 to `n` (input from user).

**Student solution:**

```python
n = int(input('Enter n: '))
sum = 0
for i in range(1, n+1):
    sum += i
print('Sum =', sum)
```

**Exercise 3:** Ask the user to guess a number (1 to 5). If guessed correctly, print "Correct" and stop.

**Student solution:**

```python
secret = 3
while True:
    guess = int(input('Guess (1-5): '))
    if guess == secret:
        print('Correct')
        break
    else:
        print('Try again')
```

**Exercise 4 (medium):** Given a list of numbers, print only the positive ones using `continue`.

**Student solution:**

```python
nums = [-2, 3, 0, -1, 5]
for x in nums:
    if x <= 0:
        continue
    print(x)
```

Answers provided so students or teacher can check quickly.

---

## 13. Teaching tips and assessment

* Use live coding and ask students to predict output before running.
* Give short pair-programming tasks (2–3 minutes) to keep engagement.
* For assessment: give 5 multiple choice + 2 short coding tasks.

---

## Appendix — quick reference

* `for item in iterable:` — loop over items
* `while condition:` — loop while condition true
* `break` — stop loop
* `continue` — skip to next iteration
* `pass` — placeholder
* `range(start, stop, step)` — generate sequence

---

If you want, I can:

* Export this README as a `.md` file ready to download,
* Add more student exercises (easy/medium/hard),
* Convert it to a printable handout or slides.

Happy teaching! 👩‍🏫👨‍🏫
