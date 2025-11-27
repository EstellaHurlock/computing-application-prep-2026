# computing-application-prep-2026
cd "/Users/estella/git-practice/app-prep/computing-application-prep-2026"

mkdir -p algorithms maths/evidence

# README.md 
cat > README.md <<'EOF'
# MSc – Prep Portfolio

This repository tracks my short sprint prep for university: maths fundamentals and core algorithms, plus small Python snippets.
You can find the first month of study log entries at MONTH_1_STUDY_LOG

## Structure
- `Computer Science/` – CS50: Introduction to Computer Science (changed from last weeks algorithms as I need to build my fundamentals foundations)
- `algorithms/` – small Python implementations (e.g., Gram–Schmidt).
- `maths/` – concise notes and scanned handwritten evidence.
- `STUDY_LOG.md` – dated entries of what I covered and produced.

EOF

# Study log
cat > STUDY_LOG.md <<'EOF'
# Study Log

## 2025-11-19
**Focus** python

**Topics covered**
- modules
- 2
- 3

**Learning Objective**

**Reflection**

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~x hours total (updated)

- **What is a module**: A module is any file with a .py extension. But more ideally, a module contains statements, functions, and class definitions that revolve around a similar purpose.
By default, Python comes with over 200 modules that we can use. Examples include, random, math, datetime
- **2**: text here


## Code examples: 
- **Title**
```python
s = "Python syntax highlighting"
print s
```


## 2025-11-18
**Focus** c#

**Topics covered**
- Overloaded methods
- IntelliSense

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~91 hours total (updated)

- **Use is VSC**: make sure to save in between dotnet run because otherwise it wont run the new code properly.
- **Overloaded methods**: An overloaded method signature, among other things, enables you to call the method with or without arguments specified in the calling statement. Essentially an overloaded method is defined with multiple method signatures. Overloaded methods provide different ways to call the methods or provide different types of data. 
An example is Console.WriteLine() which has 19 different overloaded versions. Most of these allow the method to accept different types and then write the specifies information to the console. Consider the following:
 ```c#
  int number = 7;
  string text = "seven";
  
  Console.WriteLine(number);
  Console.WriteLine();
  Console.WriteLine(text);
  
```
 In this example, you're invoking three separate overloaded versions of the WriteLine()method. The first WriteLine() method uses a method signature that defines an int parameter, the second uses a method dignature that defines zero parameters and the third a string parameter. Another example, the Random.Next() method has overloaded versions that enable you to set various levels of constraint on the randomly generated number.

- **IntelliSense**: As I type I'll be given clues about where to go. Identifiers. For dice.Next() In this case, IntelliSense provides all of the information that you need to select the appropriate overload, including a detailed explanation of maxValue and minValue. However, you might encounter situations where you need to consult the method's documentation. When you type ( in that line, opetions for 1/3 2/3 and 3/3 come up.


## Code examples: 
- **Random dice ranges**
```c#
Random dice = new Random();
int roll1 = dice.Next();
int roll2 = dice.Next(101);
int roll3 = dice.Next(50, 101);

Console.WriteLine($"First roll: {roll1}");
Console.WriteLine($"Second roll: {roll2}");
Console.WriteLine($"Third roll: {roll3}");
//Here the first roll doesn’t set a boundary, the second sets an upper boundary and the third an upper and lower.
```
- **larger value**
```c#

int firstValue = 500;
int secondValue = 600;
int largerValue = Math.Max(firstValue, secondValue);
Console.WriteLine(largerValue);
// found throuh intellisense
```


## 2025-11-17
**Focus** C#

**Topics covered**
- Call methods from the .NET Class Library using C# 
- stateful vs stateless
- creating instances

**Learning Objective**
To know how to find classes and methods in the .NET Class Library, and how to use them to perform common programming tasks.
**Reflection**
So far into this odule, lot's of theory to tackle here, but these are the exact sort of basics I want to get right into by bones, specifically instance methods, I have heard them mentioned in alternative research in computer science, talks and videos, so I really want to get to grips with them. feel pretty confident about using dotnet run. straightforwards. 

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~90 hours total (updated)

- **Class libraries**: the .NET Class Library includes the Console class for developers working on console applications. The Console class includes methods for input and output operations such as Write(), WriteLine(), Read(), ReadLine(), and many others. Additionally C# data types (such as string and int) are actually made available through classes in the .NET Class Library. 
- **Running VSC c# code**:Working VSC code, 
After opening my files and projects, and inputting some code: Save then Right-Click on the project in the explorer menu, then select open integrated terminal. To then run the code, type dotnet run.
- **Stateful vs stateless**
stateless methods are implemented so that they can work without referencing or changing any values already stored in memory. Stateless methods are also known as static methods.
For example, the Console.WriteLine() method doesn't rely on any values stored in memory. It performs its function and finishes without impacting the state of the application in any way.
stateful methods are built in such a way that they rely on values stored in memory by previous lines of code that have already been executed. Or they modify the state of the application by updating values or storing new values in memory. They're also known as instance methods.
Stateful (instance) methods keep track of their state in fields, which are variables defined on the class. Each new instance of the class gets its own copy of those fields in which to store state.
A single class can support both stateful and stateless methods. However, when you need to call stateful methods, you must first create an instance of the class so that the method can access state.
- **Creating an instance of a class**
To create a new instance of a class, you use the new operator. Consider the following line of code that creates a new instance of the Random class to create a new object called dice:
```c#
Random dice = new Random();
```
Comment: The latest version of the .NET Runtime enables you to instantiate an object without having to repeat the type name (target-typed constructor invocation). For example, the following code will create a new instance of the Random class:
```c#
Random dice = new();
```
- **Return values and parameters of methods**
Some methods are designed to complete their function and end "quietly". In other words, they don't return a value when they finish. They are referred to as void methods. Other methods are designed to return a value upon completion. The return value is typically the result of an operation. A return value is the primary way for a method to communicate back to the code that calls the method.
When calling a method that returns a value, you'll often assign the return value to a variable. That way, you can use the value later in your code. In the dice scenario, you assigned the return value of Random.Next() to the roll variable:
```c#
int roll = dice.Next(1, 7);
```
Even though a method returns a value, it's possible to call the method without using the return value. For example, you could ignore the return value by calling the method as follows:
```c#
dice.Next(1, 7);
```
However, ignoring the return value would be pointless. The reason you're calling the Next() method is so that you can retrieve the next random value.

- **Method parameters and arguments in the calling statement**
Methods use a method signature to define the number of parameters that the method will accept, as well as the data type of each parameter. The coding statement that calls the method must adhere the requirements specified by the method signature. Some methods provide options for the number and type of parameters that the method accepts. TBC tomo.



## Code examples: 
- **Random dice throw**
```c#
Random dice = new Random();
int roll = dice.Next(1, 7);
Console.WriteLine(roll);

//On the third code line, I include a reference to the Console class and call the Console.WriteLine() method directly. However, I use a different technique for calling the Random.Next() method. The reason why I'm using two different techniques is because some methods are "stateful" and others are "stateless".
```

## 2025-11-16
**Focus** python challenge packs

**Topics covered**
- functions python 

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~89 hours total (updated)

- **Returning values in the print text**: example below called kda.
- **moon phase example**: Here there were a few things I reminded and reinforced for myself. Paticularly with the use of return for saving each if and elif option, i was origionally using print, mainly due to habit. But it makes complete sense to use return. Additionally, within the if and elif statements, using phase instead of moon_phase, the latter is the defined fucnction name so would not make sense to use, however, the former is the actual parameter that we're using so need to add that instead. other than these small errors, it was a straightforward question.
- **making my def functions more efficient**: It's not hard to streamline the defined functions, you can put it all into one return line. this felt more necessary in the last question as I was working with string and int variables and can only return once. therefore putting it all in one line was very nice.


## Code examples: 
- **kda**
```python
def KDA(kill, death, assist):
  return(kill + assist)/death

print(f"Your average is {KDA(6, 5, 4)}")
```
- **moon phase with lots of return and if statements**
```py
def moon_phase(phase):
  
  if phase == 'New Moon':
    return "🌑"
  elif phase == 'Waxing Crescent':
    return "🌒"
  elif phase == 'First Quarter':
    return "🌓"
  elif phase == 'Waxing Gibbous':
    return "🌔"
  elif phase == 'Full Moon':
    return "🌕"
  elif phase == 'Waning Gibbous':
    return "🌖"
  elif phase == 'Last Quarter':
    return "🌗"
  elif phase == 'Waning Crescent':
    return "🌘"
  else:
    return "Invalid moon phase"
  

answer = moon_phase('New Moon')
print(answer)  

```
- **dog years, streamlined**
```py
def dog_years(name, age):
  return f"{name} is {age * 7} years old in human years."

print(dog_years('Landon', 3))
print(dog_years('Red Bean', 6))
print(dog_years('Cooper', 2))
```

## 2025-11-11
**Focus** python

**Topics covered**
- python challenge packs functions

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~88 hours total (updated)

- **return vs print**: when defining and creaating functions, no need to return unless i need the updates data to continue on, or if i'm just trying to write to the reader, do print. over complecated an example in code examples below


## Code examples: 
- **Simple functions challenge, Correct answer first then overcomplicated after**
```python
def greetings(first_name, last_name):
    print(f"{last_name}, {first_name} {last_name}")

greetings("James", "Bond")
```
With just Print, below i used return.
```py
first_name = input("first name? ")
last_name = input("last name? ")

def greetings(f, l):
  return f"{l}, {f} {l}"

print(greetings(first_name, last_name))

```

- **Return with average of parameters**
```py
def average(num1, num2):
  return (num1 + num2) / 2

result_av = average(3, 7)
print(f"The average is {result_av}")

```

## 2025-11-10
**Focus** Recaps after holiday

**Topics covered**
- Python
- C#
- C++

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~87 hours total (updated)

- **Python recaps**: reminder
```py
import random
number = random.randint(0, 6)
or
5 ** 3 
print("5^3")
or
!= 
print("not equal to")
or
for i in range(10, 0, -1):
  print(i)
print("count down from 10 to 1 increments of -1, e.g 10, 9, 8, 7 etc to 1)
```
while loops, e.g
```py
while total != 2:
  print("Nope")
or
for i in range(1, 25):
  print("* " * i)
print("dont forget hashtag for notes")
#this for i in range part means to print out an asterisk for every line of I, with a space. 
#e.g 
#*
#* *
#* * *
#* * * * etc.
for i in range(1, number + 1):
    total += i**2
#does for example 5 input, 1squared add 2 squared up to 5 squared.
class City:
  def __init__(self, name, country, population, landmarks):
    self.name = name
```

- **C# recaps**: sololearn
- **C++**: sololearn


## 2025-10-30
**Focus** c# 

**Topics covered**
- visual studio code c# setup
- c++

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~86 hours total (updated)

- **Extensions, .NET**: dotnet build, dotnet run. lots of debugging but should be setup now.
- **compile, execute**: The whole process should look like this:
Write some code.
Save the program.
Compile & execute.
Repeat.
The source code files have the extension .cpp like calculator.cpp.
The machine code files have the extension .out like calculator.out.
To compile a file, we need to type g++ followed by the file name and press enter:
example
```cpp
g++ hello.cpp
```
To execute a machine code file, we need to type ./ and the machine code file name and press enter.
```cpp
./a.out
```

note going on holiday ater today, only focusing on audio projects


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
