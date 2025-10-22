# computing-application-prep-2026-imperial
cd "/Users/estella/git-practice/imperial-app-prep/computing-application-prep-2026-imperial"

mkdir -p algorithms maths/evidence

# README.md 
cat > README.md <<'EOF'
# Imperial MSc Computing (Conversion) – Prep Portfolio

This repository tracks my short sprint prep for Imperial: maths fundamentals and core algorithms, plus small Python snippets.
You can find the first month of study log entries at MONTH_1_STUDY_LOG

## Structure
- `Computer Science/` – CS50: Introduction to Computer Science (changed from last weeks algorithms as I need to build my fundamentals foundations)
- `algorithms/` – small Python implementations (e.g., Gram–Schmidt).
- `maths/` – concise notes and scanned handwritten evidence.
- `STUDY_LOG.md` – dated entries of what I covered and produced.

# computing-application-prep-2026-imperial
cd "/Users/estella/git-practice/imperial-app-prep/computing-application-prep-2026-imperial" 

EOF

# Study log
cat > STUDY_LOG.md <<'EOF'
# Study Log

## 2025-10-22
**Focus** python. sololearn c++ intro.

**Topics covered**
- Creating a function

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** 77 hours total (updated)

- **DRY**: “Don't Repeat Yourself” (DRY) is a principle in software development aimed at reducing repetition and writing good clean code. Functions play a big part.
- **Creating a function step 1**:first you need to define your function with def. followed by the function name, a set of parentheses, and a colon, in that order.
```python
def name():
  # The code inside
```
- **naming and calling function**: The common naming convention for functions is snake_case. 
```python
def say_hello():
  print('Howdy! 🤠')
  print('How are you?')
```
this doesn't work till we add the call to say_hello
```python
def say_hello():
  print('Howdy! 🤠')
  print('How are you?')

say_hello()
```
- **inputs into a created function**: Sometimes, we want our functions to perform a specific task, but the task varies depending on different input(s). And that's where parameters come in.
Parameters are just a fancy word for input. They are variables that a functions takes in. They go inside the parentheses in the function definition and are used inside the function.
For example:
```python
name = input("Whats your name?: ")
def happy_birthday(name):
  print('Happy birthday to you')
  print('Happy birthday to you')
  print('Happy birthday dear ' + name )
  print('Happy birthday to you')

happy_birthday(name)
```
above isnt technically correct here because you can add an argument inside the call.
```py
def happy_birthday(name):
  print('Happy birthday to you')
  print('Happy birthday to you')
  print('Happy birthday dear ' + name )
  print('Happy birthday to you')

happy_birthday('Lillian')
```
- **Python return values**: every Python function has an output! The return keyword is used to terminate a function and output a value: When not added, Python will return the default value, None, as the return value.
Use return in a function when you want to send value(s) from one point in the code to another.
Use print() in a function when you want to display some text to the user.
good example exercise below called return.

## Code examples: 

- **function ecploration**
```python
print() 
#Print objects to the text stream file, separated by sep and followed by end. sep, end, file, and flush, if present, must be given as keyword arguments.
len() 
#find out number of items in a list
max() 
#find the maximum value item in a list.
range() 
#Rather than being a function, range is actually an immutable sequence type, as documented in Ranges and Sequence Types — list, tuple, range.
compile() 
#turns Python code (as text) into something Python can run (bytecode). 
```

- **area calculator**
```python
# calculator.py

import math
shape = int(input("Which shape:"  ))


if shape == 1:
  Base = int(input("Base:" ))
  Height = int(input("Height:"  ))
  area = (Base * Height) / 2
elif shape == 2:
  Base = int(input("Base:" ))
  Height = int(input("Height:"  ))
  area = Base * Height
elif shape == 3:
  Base = int(input("Base:" ))
  Height = int(input("Height:"  ))
  area = Base ** 2
elif shape == 4:
  Base = int(input("Base:" ))
  Height = int(input("Height:"  ))
  area = math.pi * (Base / 2) ** 2 
else:
  print("Quit")

print(area)
```

- **creating function**

```python
# fortune_cookie

def fortune_cookie():
  import random
  fortune = random.randint(1, 8)

  if fortune == 1:
    print("Don't pursue happiness – create it.")
  elif fortune == 2:
    print("All things are difficult before they are easy.")
  elif fortune == 3:
    print("The early bird gets the worm, but the second mouse gets the cheese.")
  elif fortune == 4:
    print("Someone in your life needs a letter from you.")
  elif fortune == 5:
    print("Don't just think. Act!")
  elif fortune == 6:
    print("Your heart will skip a beat.")
  elif fortune == 7:
    print("The fortune you search for is in another cookie.")
  else:
    print("Help! I'm being held prisoner in a Chinese bakery!")

fortune_cookie()
```

- **calling functions challenge**

```py
def distance_to_miles(distance):
  miles = distance / 1.609
  print(miles)
distance_to_miles(1000)
```

- **return**
```py
# calculator.py
def add(a, b):
  return a + b

def subtract(a, b):
  return a - b

def multiply(a, b):
  return a * b

def divide(a, b):
  return a / b

def exp(a, b):
  return a ** b

print(add(3, 5))
print(subtract(3, 5))
print(multiply(3, 5))
print(divide(3, 5))
print(exp(3, 5))
```