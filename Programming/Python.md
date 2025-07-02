# Python Beginner Cheatsheet

---

## `print()` Output data to the console
```python
# Print any text or variable
print('Hello World')
print(1000)
print(True)

# Even expressions can be printed
print(2 + 2)  # Output: 4
```

---

## Comments - Used for documentation
```python
username = 'Lovelace'  # I'm a comment
```

---

## Variables - Store data for later use
```python
acceleration = 'Δ velocity / Δ time'
gravity = 9.81

print(gravity)  # Output: 9.81
```

---

## Data Types - Specify the type variable
```python
# Integer
secret_number = 42

# Float
pi = 3.14

# String
greeting = 'Hi bestie!'

# Boolean
earth_is_flat = False
```

---

## Arithmetic Operations - Everyday math operations
```python
# Addition
sum = 10 + 12

# Subtraction
difference = 30 - 8

# Multiplication
product = 24 * 0.75

# Division
quotient = 81 / 9

# Modulus
remainder = 76 % 4

# Exponents
exponent = 2 ** 3
```

---

## `input()` - Grab user input
```python
username = input('Enter your name: ')
age = int(input('Enter your age: '))
```

---

## Control Flow - Test condition for truth
```python
if grade >= 90:
    print('A')
elif grade >= 80:
    print('B')
elif grade >= 70:
    print('C')
else:
    print('D')
```

---

## Relational Operators - Compare two values
```python
a == b  # Equal to
a != b  # Not equal to
a < b   # Less than
a <= b  # Less than or equal to
a > b   # Greater than
a >= b  # Greater than or equal to
```

---

## Logical Operators - Combine two conditions
```python
a and b  # True if both are True
a or b   # True if at least one is True
not a    # True if a is False
```

---

## Random - Generate a random number
```python
import random
num = random.randint(1, 9)
```

---

## Loops - Run code over and over

### `while` loop
```python
while coffee < 1:
    print('Tired')
```

### `for` loop
```python
for i in range(10):
    print(i)
```

---
