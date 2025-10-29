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

## 2025-10-28
**Focus** python, c# 

**Topics covered**
- create classes for data types in lists
- create objects
-  The __ init __() Method
- instance methods

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~84 hours total (updated)

- **classes**: For example if i have a list here of student_1 = [1001, 'Asiqur', 10, 3.7, True], how would we know what each item corresponds to, therefore we make classes. heres how a class is made
```py
# restaurants.py food delivery
class Restaurant:
  name = '' #str
  category = '' #str
  rating = 0.0 #decimal
  delivery = False #bool

```

- **objects**: An object is an "instance" of a class. A class is simply a template for creating objects, which are individual copies of the class with actual values.
here is an example with the restaurant. vars function is a built in function with definition 'Return the __dict__ attribute for a module, class, instance, or any other object with a __dict__ attribute.'
```py
class Restaurant:
  name = ''
  category = ''
  rating = 0.0
  delivery = False

bobs_burgers = Restaurant()
bobs_burgers.name = 'Bob\'s Burgers'
bobs_burgers.category = 'American Diner'
bobs_burgers.rating = 4.2
bobs_burgers.delivery = False

Marse_Nepalese = Restaurant()
Marse_Nepalese.name = 'Marse, ancient grains'
Marse_Nepalese.category = 'Takeaway'
Marse_Nepalese.rating = 5.0
Marse_Nepalese.delivery = False

Akara = Restaurant()
Akara.name = 'Akara'
Akara.category = 'West African Restaurant'
Akara.rating = 5.0
Akara.delivery = False

print(vars(bobs_burgers))
print(vars(Marse_Nepalese))
print(vars(Akara))
#prints out: {'name': "Bob's Burgers", 'category': 'American Diner', 'rating': 4.2, 'delivery': False}
#{'name': 'Marse, ancient grains', 'category': 'Takeaway', 'rating': 5.0, 'delivery': False}
#{'name': 'Akara', 'category': 'West African Restaurant', 'rating': 5.0, 'delivery': False}

```
- **The __ init __() Method**: Using the init method lets us construct objects with unique attributes, we can pass in values for each attribute to initialize the new object, all in a single line!
class City:
  def __init__(self, name, country, population, landmarks):
    self.name = name
    self.country = country
    self.population = population
    self.landmarks = landmarks
- **Instance methods**: Just like how insert(), append() and remove() are built in methods here you will be adding your own methods, within a class. 

## Code examples: 
- **Objects and Classes**
```python
class City:
  def __init__(self, name, country, population, landmarks):
    self.name = name
    self.country = country
    self.population = population
    self.landmarks = landmarks
Beijing = City('Beijing', 'China', 21858000, "forbidden city, Great Wall, Temple of Heaven")
London = City('London', 'United Kingdom', 8945000, 'St Pauls, Westminster, 02')
Taipei = City('Taipei', 'Taiwan', 2447000, 'Lungshan Temple, 101 Observatory, Ximending')


print(vars(Beijing))
print(vars(London))
print(vars(Taipei))
```

- **instance method example**
```py
class Student: 
  def __init__(self, name, year, enrolled, gpa):
    self.name = name
    self.year = year
    self.enrolled = enrolled
    self.gpa = gpa
  
  def display_info(self):
    print('The student ' + self.name + '\'s GPA is ' + str(self.gpa) + '!')
  
  def graduation(self):
    if self.enrolled and self.gpa > 2.5 and self.year == 12:
      print(self.name + ' will be able to graduate this year!')

mitsuha = Student('宮水三葉', 12, True, 4.0)
taki = Student('立花瀧', 11, True, 3.8)

mitsuha.display_info()
mitsuha.graduation()
taki.display_info()
taki.graduation()
# Output:
# The student 宮水三葉's GPA is 4.0!
#宮水三葉 will be able to graduate this year!
# The student 立花瀧's GPA is 3.8!
```
```py
# bank_accounts.py

class BankAccount:
    def __init__(self, first_name, last_name, account_id, account_type, pin, balance):
        self.first_name = first_name
        self.last_name = last_name
        self.account_id = account_id
        self.account_type = account_type
        self.pin = pin
        self.balance = balance

    def deposit(self):
        deposit_amount = float(input("Amount to deposit: "))
        self.balance += deposit_amount
        print(self.balance)

    def withdraw(self):
        withdraw_amount = float(input("How much do you wish to withdraw?: "))
        self.balance -= withdraw_amount
        print(self.balance)

    def display_balance(self):
        print(self.balance)

person = BankAccount('Estella', 'Hurlock', 1234567, 'bank', 1234, 67.99)
person.deposit()
person.withdraw()
person.display_balance()

```

```py
#pokedex practice instance methods
# pokedex.py

class Pokemon:
  def __init__(self, entry, name, types, description, is_caught):
    self.entry = entry
    self.name = name
    self.types = types
    self.description = description
    self.is_caught = is_caught
  
  def speak(self):
    print(self.name, self.name)
  
  def display_details(self):
    print(
      f"Entry Number: {self.entry}\n" 
      f"Name: {self.name}\n" 
      f"Type: {self.types}\n" 
      f"Description: {self.description}"
      )
    if self.is_caught:
      print(f"{self.name} 'has already been caught!")
    else:
      print(f"{self.name} has not been caught yet!")

Pikachu = Pokemon(23, 'Pikachu', 'Electric', 'It has small electric sacs on both its cheeks. If threatened, it looses electric charges from the sacs.', True)
Arceus = Pokemon(493, 'Arceus', 'Normal', 'Cool Pokemon, mythical white equine', True)
Umbreon = Pokemon(197, 'Umbreon', 'Dark', "Dark evee evolution, beautiful majestic awesomness", True)


Pikachu.speak()
Pikachu.display_details()
Arceus.speak()
Arceus.display_details()
Umbreon.speak()
Umbreon.display_details()
```


## 2025-10-27
**Focus** python, c#, c++

**Topics covered**
- very simple time series analysis
- lambda
- c# project grade assignments, Write Your First Code Using C# trophy achieved.
- C++ catchup of sollolearn to codedex.

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~81 hours total (updated)

- **simple time series analysis**: Time series analysis involves working with data ordered by time, such as stock prices. In the exercise below, I practiced accessing and summarizing values in a list using functions like price_at, max_price, and min_price. Python lists use 0-based indexing, so converting to 1-based indices requires i-1. Using loops and built-in functions like max() and min(), you can find the highest or lowest values over a given range. These basics build a foundation for more advanced time series work using tools like pandas.
- **lambda**: In Python, lambdas provide a quick way to define small functions. Lambda functions (also known as anonymous functions) are concise functions defined without a name. They are often used for short-lived tasks where a full function definition might seem verbose or unneeded. First, we use the reserved lambda keyword to begin defining the function. Then, we can use one or more arguments (separated by commas), followed by a : colon. On the other side of the colon is the expression that may use the arguments to produce an output.

regular
```py
def double(x):
  return x * 2
```
with lambda
```py
double = lambda x: x * 2

print(double(4))
# Output: 8
```
```py
numbers = [1, 2, 3, 4, 5]

tripled_numbers = list(map(lambda x: x * 3, numbers))

odd_numbers = list(filter(lambda x: x % 2 == 1, numbers))

print(tripled_numbers)  # Output: [3, 6, 9, 12, 15]
print(odd_numbers)      # Output: [1, 3, 5]

#OR

names = ['Anthony', 'Benedict', 'Colin', 'Daphne', 'Eloise']

filtered_names = list(filter(lambda name: name[0].upper() != 'A', names))

print(filtered_names)   # Output: ['Benedict', 'Colin', 'Daphne', 'Eloise']

#OR

compound_word = lambda str1, str2: str1 + str2

word = compound_word('fire', 'fly')

print(f'The compound word is: {word}')
```
- **c# grade at school code**: to check things arre working fine in the NET editor, progess is checked with a Console.WriteLine, however in visual studio code, you can check variables and their updates specially. at the bottom of the code with the Console.Writeline() ending. the \t helps to space correctl and the/n is for the new line. project most helpful for formatting.
- **gpa c# code**: when getting decimals which are many digits into a set number, do leading digit int, first digit int by *10 then %10 then second digit *100 %100 etc. here example is 3.35437498437628476539287 to 3.35. 
- **C++ catchup notes from sololearn to codedex**: memory management, object-oriented programming. single line comments and multi line comments. single line // multi line /* to */.



## Code examples: 
- **Title**
```python
stock_prices = [34.68, 36.09, 34.94, 33.97, 34.68, 35.82, 43.41, 44.29, 44.65, 53.56, 49.85, 48.71, 48.71, 49.94, 48.53, 47.03, 46.59, 48.62, 44.21, 47.21]

def price_at(i):
  return stock_prices[i-1]

def max_price(a, b):
  maxim = price_at(a)
  for i in range(a, b + 1):
    maxim = max(maxim, price_at(i))
  return maxim

def min_price(a, b):
  minim = price_at(a)
  for i in range(a, b + 1):
    minim = min(minim, price_at(i))
  return minim

print(max_price(1, 20))
print(min_price(1, 20))
print(price_at(6))
```
optional:
```py
stock_prices = [34.68, 36.09, 34.94, 33.97, 34.68, 35.82, 43.41, 44.29, 44.65, 53.56, 49.85, 48.71, 48.71, 49.94, 48.53, 47.03, 46.59, 48.62, 44.21, 47.21]

def price_at(i):
  return stock_prices[i-1]

def max_price(a, b):
    return max(stock_prices[a-1:b]) 

def min_price(a, b):
    return min(stock_prices[a-1:b])

print(max_price(1, 20))
print(min_price(1, 20))
print(price_at(6))
```
condensed, more efficient. 

```py
# drive_thru.py
menu = ['🍔 Cheeseburger', '🍟 Fries', '🥤 Soda', '🍦 Ice Cream', '🍪 Cookie']

print(
    "Welcome to Sonnyboy's Diner!\n"
    "Here's the menu:\n"
    "1. 🍔 Cheeseburger\n"
    "2. 🍟 Fries\n"
    "3. 🥤 Soda\n"
    "4. 🍦 Ice Cream\n"
    "5. 🍪 Cookie"
)

def value_at(i):
    return menu[i - 1] 
    
get_item = int(input("What number would you like? "))
print(value_at(get_item))

```
```c#
// initialize variables - graded assignments 
int currentAssignments = 5;

int sophia1 = 93;
int sophia2 = 87;
int sophia3 = 98;
int sophia4 = 95;
int sophia5 = 100;

int nicolas1 = 80;
int nicolas2 = 83;
int nicolas3 = 82;
int nicolas4 = 88;
int nicolas5 = 85;

int zahirah1 = 84;
int zahirah2 = 96;
int zahirah3 = 73;
int zahirah4 = 85;
int zahirah5 = 79;

int jeong1 = 90;
int jeong2 = 92;
int jeong3 = 98;
int jeong4 = 100;
int jeong5 = 97;

int sophiaSum = sophia1 + sophia2 + sophia3 + sophia4 + sophia5;
int nicolasSum = nicolas1 + nicolas2 + nicolas3 + nicolas4 + nicolas5;
int zahirahSum = zahirah1 + zahirah2 + zahirah3 + zahirah4 + zahirah5;
int jeongSum = jeong1 + jeong2 + jeong3 + jeong4 + jeong5;

decimal sophiaScore = (decimal) sophiaSum / currentAssignments;
decimal nicolasScore = (decimal) nicolasSum / currentAssignments;
decimal zahirahScore = (decimal) zahirahSum / currentAssignments;
decimal jeongScore = (decimal) jeongSum / currentAssignments;

Console.WriteLine("Student\t\tGrade\n");
Console.WriteLine("Sophia:\t\t" + sophiaScore + "\tA");
Console.WriteLine("Nicolas:\t" + nicolasScore + "\tB");
Console.WriteLine("Zahirah:\t" + zahirahScore + "\tB");
Console.WriteLine("Jeong:\t\t" + jeongScore + "\tA");
```

```c#
//student gpa
string studentName = "Sophia Johnson";
string course1Name = "English 101";
string course2Name = "Algebra 101";
string course3Name = "Biology 101";
string course4Name = "Computer Science I";
string course5Name = "Psychology 101";

int course1Credit = 3;
int course2Credit = 3;
int course3Credit = 4;
int course4Credit = 4;
int course5Credit = 3;

int gradeA = 4;
int gradeB = 3;

int course1Grade = gradeA;
int course2Grade = gradeB;
int course3Grade = gradeB;
int course4Grade = gradeB;
int course5Grade = gradeA;

int totalCreditHours = 0;
totalCreditHours += course1Credit;
totalCreditHours += course2Credit;
totalCreditHours += course3Credit;
totalCreditHours += course4Credit;
totalCreditHours += course5Credit;

int totalGradePoints = 0;
totalGradePoints += course1Credit * course1Grade;
totalGradePoints += course2Credit * course2Grade;
totalGradePoints += course3Credit * course3Grade;
totalGradePoints += course4Credit * course4Grade;
totalGradePoints += course5Credit * course5Grade;

decimal gradePointAverage = (decimal) totalGradePoints/totalCreditHours;

int leadingDigit = (int) gradePointAverage;
int firstDigit = (int) (gradePointAverage * 10) % 10;
int secondDigit = (int) (gradePointAverage * 100 ) % 10;

Console.WriteLine($"Student: {studentName}\n");
Console.WriteLine("Course\t\t\t\tGrade\tCredit Hours");

Console.WriteLine($"{course1Name}\t\t\t{course1Grade}\t\t{course1Credit}");
Console.WriteLine($"{course2Name}\t\t\t{course2Grade}\t\t{course2Credit}");
Console.WriteLine($"{course3Name}\t\t\t{course3Grade}\t\t{course3Credit}");
Console.WriteLine($"{course4Name}\t{course4Grade}\t\t{course4Credit}");
Console.WriteLine($"{course5Name}\t\t{course5Grade}\t\t{course5Credit}");

Console.WriteLine($"\nFinal GPA:\t\t\t {leadingDigit}.{firstDigit}{secondDigit}");

```

a lot of code that has potential to be condensed down significantly for both of these.

## 2025-10-23 - 2025-10-26 
- **sololearn c++**


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
