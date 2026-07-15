# String Case Conversions in Python

String case conversion questions are very common in placement interviews.

The easiest way to solve all of them is to follow this **3-step approach**:

```text
Input String
      │
      ▼
Split the sentence into words
      │
      ▼
Modify each word
      │
      ▼
Join the words in the required format
```

---

# Example Input

```text
hello world python
```

---

# 1. Title Case

## Definition

Convert the **first letter of every word** to uppercase while keeping spaces.

---

## Input

```text
hello world python
```

## Output

```text
Hello World Python
```

---

## Algorithm

1. Read the string.
2. Split the sentence into words.
3. Capitalize every word.
4. Join the words with spaces.
5. Print the result.

---

## Python Code

```python
s = input()

words = s.split()

result = ""

for word in words:
    result += word.capitalize() + " "

print(result.strip())
```

---

## Dry Run

```text
Input

hello world python

↓

Split

['hello', 'world', 'python']

↓

Capitalize

Hello
World
Python

↓

Join

Hello World Python
```

---

## Time Complexity

```text
O(n)
```

---

# 2. Camel Case

## Definition

- First word starts with lowercase.
- Remaining words start with uppercase.
- No spaces.

---

## Input

```text
hello world python
```

## Output

```text
helloWorldPython
```

---

## Algorithm

1. Read the string.
2. Split into words.
3. Keep the first word in lowercase.
4. Capitalize remaining words.
5. Join without spaces.
6. Print the result.

---

## Python Code

```python
s = input()

words = s.split()

result = words[0].lower()

for i in range(1, len(words)):
    result += words[i].capitalize()

print(result)
```

---

## Dry Run

```text
Split

['hello', 'world', 'python']

↓

First Word

hello

↓

Capitalize Remaining

World
Python

↓

Join

helloWorldPython
```

---

## Time Complexity

```text
O(n)
```

---

# 3. Pascal Case

## Definition

Every word starts with uppercase.

No spaces are present.

---

## Input

```text
hello world python
```

## Output

```text
HelloWorldPython
```

---

## Algorithm

1. Read the string.
2. Split into words.
3. Capitalize every word.
4. Join without spaces.
5. Print the result.

---

## Python Code

```python
s = input()

words = s.split()

result = ""

for word in words:
    result += word.capitalize()

print(result)
```

---

## Dry Run

```text
Split

['hello', 'world', 'python']

↓

Capitalize

Hello
World
Python

↓

Join

HelloWorldPython
```

---

## Time Complexity

```text
O(n)
```

---

# 4. Snake Case

## Definition

Convert every word to lowercase.

Replace spaces with `_`.

---

## Input

```text
Hello World Python
```

## Output

```text
hello_world_python
```

---

## Algorithm

1. Read the string.
2. Convert the string to lowercase.
3. Replace every space with `_`.
4. Print the result.

---

## Python Code

```python
s = input()

print(s.lower().replace(" ", "_"))
```

---

## Dry Run

```text
Input

Hello World Python

↓

Lowercase

hello world python

↓

Replace Space

hello_world_python
```

---

## Time Complexity

```text
O(n)
```

---

# 5. Kebab Case

## Definition

Convert every word to lowercase.

Replace spaces with `-`.

---

## Input

```text
Hello World Python
```

## Output

```text
hello-world-python
```

---

## Algorithm

1. Read the string.
2. Convert the string to lowercase.
3. Replace spaces with `-`.
4. Print the result.

---

## Python Code

```python
s = input()

print(s.lower().replace(" ", "-"))
```

---

## Dry Run

```text
Input

Hello World Python

↓

Lowercase

hello world python

↓

Replace Space

hello-world-python
```

---

## Time Complexity

```text
O(n)
```

---

# Comparison Table

| Case Type | Output |
|------------|---------------------|
| Title Case | Hello World Python |
| Camel Case | helloWorldPython |
| Pascal Case | HelloWorldPython |
| Snake Case | hello_world_python |
| Kebab Case | hello-world-python |

---

# Visual Representation

```text
Input

hello world python

                Split()
                   │
                   ▼
      ['hello','world','python']
                   │
    ┌──────────────┼───────────────┐
    │              │               │
    ▼              ▼               ▼

Title Case     Camel Case     Pascal Case

Hello          hello          Hello
World          World          World
Python         Python         Python

Join           Join           Join
with Space     No Space       No Space

↓

Hello World Python
helloWorldPython
HelloWorldPython

-----------------------------------------

Snake Case

Lowercase

↓

hello world python

↓

Replace Space with "_"

↓

hello_world_python

-----------------------------------------

Kebab Case

Lowercase

↓

hello world python

↓

Replace Space with "-"

↓

hello-world-python
```

---

# Common Functions Used

| Function | Purpose |
|----------|---------|
| `split()` | Splits a sentence into words |
| `capitalize()` | Makes the first letter uppercase |
| `lower()` | Converts all letters to lowercase |
| `replace()` | Replaces one character with another |
| `join()` | Joins multiple words into one string |
| `strip()` | Removes leading/trailing spaces |

---

# Interview Tips

✅ **Title Case**
- Keep spaces.
- Capitalize every word.

✅ **Camel Case**
- First word starts with lowercase.
- Remaining words start with uppercase.
- No spaces.

✅ **Pascal Case**
- Every word starts with uppercase.
- No spaces.

✅ **Snake Case**
- Convert to lowercase.
- Replace spaces with `_`.

✅ **Kebab Case**
- Convert to lowercase.
- Replace spaces with `-`.

---

# Easy Trick to Remember

```text
Sentence
      │
      ▼
split()
      │
      ▼
['hello', 'world', 'python']
      │
      ▼
Modify each word
      │
      ▼
Join according to the required case

Title  → " "
Camel  → ""
Pascal → ""
Snake  → "_"
Kebab  → "-"
```
