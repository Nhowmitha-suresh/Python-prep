# 1. Sum of Digits

## Input
```
12345
```

## Output
```
15
```

## Code

```python
num = int(input())

temp = num
total = 0

while temp > 0:
    digit = temp % 10
    total += digit
    temp = temp // 10

print(total)
```
