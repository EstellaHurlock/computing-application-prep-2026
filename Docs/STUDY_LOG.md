# computing-application-prep-2026-imperial
cd "/Users/estella/git-practice/imperial-app-prep/computing-application-prep-2026-imperial"

mkdir -p algorithms maths/evidence

# README.md 
cat > README.md <<'EOF'
# Imperial MSc Computing (Conversion) – Prep Portfolio

This repository tracks my short sprint prep for Imperial: maths fundamentals and core algorithms, plus small Python snippets.

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

## 2025-10-13
**Focus** python, C#, Markdown

**Topics covered**
- Python challenge packs loops
- C# begginners funadamentals
- Markdown chetsheets and basics. 

**Work produced**
- Code snippets below

**Time:** ~67 hours total (updated)
EOF

- **Console.WriteLine**: Single quotes create a character literal. double quotation marks creates a string data type. Just like the string data type, you use char whenever you have a single alphanumeric character for presentation (not calculation).
- **Data types float, double, decimal**: 

Float Type | Precision
--- | --- 
float | ~6-9 digits
double | ~15-17 digits
decimal | 8-29 digits

Console.WriteLine(0.25F); the F is a literal suffix. float
Console.WriteLine(2.625); automatically creates double. 
Console.WriteLine(12.39816m); m is decimal literal suffix. can use lower case or upper case M.
- **Data types Booleans**
Console.WriteLine(true);
Console.WriteLine(false); as you see no quotations needed.
- **Declaring Variables**
To create a new variable, you must first declare the data type of the variable, and then give it a name.
string thisIsCamelCase;
char userOption;
int gameScore;
decimal particlesPerMillion;
bool processedCustomer;
Variable names shouldn't include the data type of the variable. You might see some advice to use a style like string strValue;. That advice is no longer current.
- **Setting the Variables**
string firstName;
firstName = "Bob"; 
or
string firstName = "Bob"; to set immediately in the same line
- **Using var**
The var keyword has an important use in C#. Many times, the type of a variable is obvious from its initialization. In those cases, it's simpler to use the var keyword. The var keyword can also be useful when planning the code for an application. When you begin developing code for a task, you may not immediately know what data type to use. Using var can help you develop your solution more dynamically.

## Code examples: 

- **Python syntax highlighting** 

```python
s = "Python syntax highlighting"
print s
```

- **text answer loop**
```python
answer = input("Are we there yet?  ")

while answer != "Yes":
    answer = input("Are we there yet?  ")

print("Yayyy")

- **Roll dice until 1 and 1**

import random

die1 = random.randint(1, 6)
die2 = random.randint(1, 6)

total = die1 + die2

while total != 2:
  print("Nope")

  die1 = random.randint(1, 6)
  die2 = random.randint(1, 6)

  total = die1 + die2
else:
  print("Snake eyes!")

- **printing challenge**
for i in range(1, 25):
  print("* " * i)
```
- **Adding Squares**

number = int(input("What is your number?: "))

total = 0
for i in range(1, number + 1):
    total += i**2

print(total)

- **C# defining variables**

```C#
string firstName = "Bob";
int messages = 3;
decimal temp = 34.4m;

Console.Write("Hello, ");
Console.Write(firstName);
Console.Write("! You have ");
Console.Write(messages);
Console.Write(" messages in your inbox. The temperature is ");
Console.Write(temp);
Console.Write(" celsius."); 
```

## 2025-10-09
**Focus:** C# Coding 

**Topics covered**
- C#

Main track: Microsoft Learn modules (daily 20–30 min). 
Microsoft Learn
Daily practice: 1–2 Exercism exercises. 
Exercism.
Milestone: Finish the freeCodeCamp × Microsoft certification to lock it in. FreeCodeCamp

**Work produced**
- Code snippets below

**Time:** ~63 hours total (updated)
EOF

- **Small things**: Console.WriteLine("Hello World!"); // creates comment, Console.Write just adds one line with multiple.
- **concepts**: Console is a class. WriteLine() is a method, "blablabla" is a string. The parentheses are known as the method invocation operator. The period is the member access operator. In other words, the dot is how you "navigate" from the class to one of its methods.

## 2025-10-08
**Focus:** Python coding

**Topics covered**
- Loops
- nested loops

**Work produced**
- Code snippets below

**Time:** ~61 hours total (updated)
EOF

- **Loops**: People will often use the generic term “iterate” when referring to loops; iterate simply means “to repeat”. Kinds of loops, while loops, for loops with range() function. 
- **Range()**: Goes for numbers from 0 so range(6) is 0 1 2 3 4 5. example for i in range(100): - print("I will not use Snapchat in class"). for moving with range range(start, stop, step): so countdown from 99 is range(99, 0, -1).
- **String interpolation**:  if you have a template for saying hello to a person in an email like 'Hi {name}, nice to meet you!', you would like to replace the placeholder {name} with an actual name. This is string interpolation. so for range looks like 
for i in range(6):
  print(f'The square of {i} is {i*i}')
- **nested loops** To break out of the for loop, we use the break keyword. To break out of the outer while loop, we reassign False to the notFound variable.


## Code examples: 
- **Pin code loop**

print('BANK OF CODÉDEX')

pin = int(input('Enter your PIN: '))

while pin != 1234:
  pin = int(input('Incorrect PIN. Enter your PIN again: '))

if pin == 1234:
  print('PIN accepted!')

- **number guess**

#guess.py

guess = 0
tries = 0

while guess != 6 and tries < 6:
  guess = int(input("Guess the number:  "))
  tries = tries + 1

if guess != 6:
  print("You ran out of tries!")
else: 
  print('You got it!')

- **99_bottles.py**

for i in range(99, 0, -1):
  print(f" {i} bottles of beer on the wall")
  print(f"{i} bottles of beer")
  print("Take one down, pass it around")
  print(f"{i-1} bottles of beer on the wall")

- **FizzBuzz challenge**

for i in range(1, 101, 1):
  if i % 3 == 0 and i % 5 != 0:
    print("Fizz")
  elif i % 5 == 0 and i % 3 != 0:
    print("Buzz")
  elif i % 3 == 0 and i % 5 == 0: 
    print("FizzBuzz")
  else:
    print(i)
NOTE could put 3 and 5 first so that they dont get caughts in the others then no need for the extra constraints.

- **nested loop example**
import random

lucky_number = random.randint(1, 9)
not_found = True

while not_found:
  for i in range(1, 10):
    if i == lucky_number:
      not_found = False
      break
    else:
      print(i)

print(f"Yay I got my lucky number {lucky_number}! 🍀")

- **Control flow challenge**

rating = 1.1

if rating >= 4.5:
    print("Extraordinary")
elif rating >= 4:
    print("Excellent")
elif rating >= 3:
    print("Good")
elif rating >= 2:
    print("Fair")
else:
    print("Poor")

- **medium controlo flow challenge**

import random
number = random.randint(0, 5)

if number == 0:
  print('Flamingos turn pink from eating shrimp.')
elif number == 1:
  print('The only food that doesn\'t spoil is honey.')
elif number == 2:
  print('Shrimp can only swim backwards.')
elif number == 3:
  print('A taste bud\'s life span is about 10 days.')
elif number == 4:
  print('It is impossible to sneeze while sleeping.')
elif number == 5:
  print('It is impossible to sneeze while sleeping.')
else:
  print("invalid")

- **Control flow harder**

pweight = float(input("What is your Earth weight? as a decimal.  "))
pnumber = int(input("What is your planet number?  "))

if pnumber == 1:      
    dweight = pweight * 0.38
    print(dweight)
elif pnumber == 2:    
    dweight = pweight * 0.91
    print(dweight)
elif pnumber == 3:  
    dweight = pweight * 0.38
    print(dweight)
elif pnumber == 4:    
    dweight = pweight * 2.53
    print(dweight)
elif pnumber == 5:   
    dweight = pweight * 1.07
    print(dweight)
elif pnumber == 6:  
    dweight = pweight * 0.89
    print(dweight)
elif pnumber == 7:   
    dweight = pweight * 1.14
    print(dweight)
else:
    print("invalid planet number")


## 2025-10-07
**Focus:** Python coding

**Topics covered**
- Python control flow
- If statements
- Relational Operators
- Randoms 
- Logical operators

**Work produced**
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-24/` (photos/scans)

**Time:** ~58 hours total (update)
EOF

- **Control flow def**:  how programs "make decisions" by evaluating different conditions, and introducing logic into program
- **If statements**: Put a colon after the entire if statement and then a colon after else. Also known as Elif. nested if statements, example in coding snippets.
- **Relational operators**: == equal to, != not equal to, > greater than, < less than, >= greater than or equal to, <= less than or equal to
- **Random integers.** import random in first from the .py file style. then assign number e.g num = random.randint(1, 9)
- **Logical Operators** also known as boolean operators. and returns True if both conditions are True, and returns False otherwise. or returns True if at least one of the conditions is True, and False otherwise. not returns True if the condition is False, and vice versa.

## Code examples: 
- **Coin flip** 
import random

num = random.randint(0, 1)   # Generates a random number that's either 0 or 1

if num > 0.5:
  print('Heads')
else:
  print('Tails')

- **Class grade** 

grade = 60

if grade >= 55:
  print('you passed')

else:
  print('you failed')

- **pH value** 

ph = int(input('Enter a pH value 0-14: '))

if ph > 7:
  print('Basic')
elif ph < 7:
  print('Acidic')
else:
  print('Neutral')

- **Magic 8 ball**

# Magic 8 Ball 🎱
# Codédex

import random

question = input('Question:      ')

random_number = random.randint(1, 9)

if random_number == 1:
  answer = 'Yes - definitely'
elif random_number == 2:
  answer = 'It is decidedly so'
elif random_number == 3:
  answer = 'Without a doubt'
elif random_number == 4:
  answer = 'Reply hazy, try again'
elif random_number == 5:
  answer = 'Ask again later'
elif random_number == 6:
  answer = 'Better not tell you now'
elif random_number == 7:
  answer = 'My sources say no'
elif random_number == 8:
  answer = 'Outlook not so good'
elif random_number == 9:
  answer = 'Very doubtful'
else:
  answer = 'Error'
  
print('Magic 8 Ball:  ' + answer)

good habit to not print in a long list of if and elifs like thi sand do answer then print instead. 

- **Theme park rides**

height = int(input('What is your height (cm)? '))
credits = int(input('How many credits do you have? '))

if height >= 137 and credits >= 10:
  print("Enjoy the ride!")
elif height < 137 and credits >= 10:
  print("You are not tall enough to ride.")
elif credits < 10 and height >= 137:
  print("You don't have enough credits to ride.")
else:
  print("You are not tall enough for this ride, nor do you have enough credits.")

- **Sorting hat**
# sortinghat.py

name = input("What is your name?: ")

q1 = int(input(" Do you like Dawn or Dusk? (Answer 1 for Dawn and 2 for Dusk) "))
q2 = int(input(" When I’m dead, I want people to remember me as?: (1 The good, 2 the great, 3 the wise, 4 the bold) "))
q3 = int(input(" Which kind of instrument most pleases your ear?: (1 The violin, 2 The trumpet, 3 The piano, 4 The drum) "))

Gryffindor = 0
Ravenclaw = 0
Hufflepuff = 0
Slytherin = 0

if q1 == 1:
  Gryffindor += 1
  Ravenclaw += 1
elif q1 == 2: 
  Hufflepuff += 1 
  Slytherin += 1
else:
  print("wrong input Q1") 

if q2 == 1:
  Hufflepuff += 2
elif q2 == 2: 
  Slytherin += 2
elif q2 == 3: 
  Ravenclaw += 2
elif q2 == 4: 
  Gryffindor += 2
else:
  print("wrong input Q2")

if q3 == 1:
  Slytherin += 4
elif q3 == 2: 
  Hufflepuff += 4
elif q3 == 3: 
  Ravenclaw += 4
elif q3 == 4: 
  Gryffindor += 4
else:
  print("wrong input Q3")

print('Gryffindor', Gryffindor)
print('Ravenclaw', Ravenclaw)
print('Hufflepuff', Hufflepuff)
print('Slytherin', Slytherin)

if Gryffindor > Ravenclaw and Gryffindor > Hufflepuff and Gryffindor > Slytherin:
  house = 'Gryffindor'
elif Ravenclaw > Gryffindor and Ravenclaw > Hufflepuff and Ravenclaw > Slytherin:
  house = 'Ravenclaw'
elif Hufflepuff > Gryffindor and Hufflepuff > Ravenclaw and Hufflepuff > Slytherin:
  house = 'Hufflepuff'
elif Slytherin > Gryffindor and Slytherin > Ravenclaw and Slytherin > Hufflepuff:
  house = 'Slytherin'
else:
  house = "wrong input"

print(name + " you are a " + house + "!")

- **Nested if statement**
weather = 'Sunny'
humidity = 35

if weather == 'Sunny':
  if humidity < 60:
    print('Let’s go to the beach! 🏖️')
  else:
    print('Hmmm, it’s a little humid for a beach day.')
else:
  print('It’s not sunny today... let’s try for another day.') 

## 2025-10-06
**Focus:** Python Codedex, Variables/ data types, operators

**Topics covered**
- Different Variables and data types
- Error types

**Work produced**
- coding snippets down below

**Time:** ~55 hours total (update)
EOF

# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-30

- **Different Variables**: Example: string value "Estella Hurlock" is assigned to (=) the variable name, or assigning number value 22 to variable age. Int (whole numbers), float(decimals), string (text) , boolean (true or false) other comment, " or' i recommend " because then i can put text with ' inside.
- **Operators**: Addition+ Subtraction- Multiplication* Division/ example, score = 4 + 3 print(score) output 8. Modulo operator % doesnt give division but gives the remainder instead. example score = 5 % 3 score is 2. Another is exponents, So 2 ** 3 is 2³. 
- **Error types**: Three most common errors are SyntaxError, NameError  and TypeError. syntax is because the syntax is wrong, name error is made from  referring to a variable that hasn't been made yet, type error is from wrong type of data presented, for example with print(message + str(28)) if you didnt have str it would confuse things. 

## Code examples: 
- **Farenheit to celcius** 
Farenheit = 70

Celsius = (Farenheit - 32) / 1.8

print(Celsius)

- **BMI**
mass = 70
height = 1.73

bmi = mass / (height ** 2)

print(bmi)

- **Pythagoras** 
a = int(input("What is your short side length?"))
b = int(input("what is the other short side length?"))

Hypotenuse = (a ** 2 + b ** 2) ** 0.5

print(Hypotenuse)
COMMENT: here my initial error was putting 0.5 ** (etc) this means putting 0.5 to the power of pythagorases theorem so wrong way round.

- **Quadratic formula** 

a = int(input("Enter a: "))
b = int(input("Enter b: "))
c = int(input("Enter c: "))

x1 = (-b + (b*b - 4*a*c)**0.5) / (2*a)
x2 = (-b - (b*b - 4*a*c)**0.5) / (2*a)

print(x1)
print(x2)

- **Currency converter**
pesos = int(input("What do you have left in pesos? "))
soles = int(input("What do you have left in soles? ")) 
reais = int(input("What do you have left in reais? "))

USD = (pesos*0.055) + (soles*0.29) + (reais*0.19)

print(USD)

## 2025-09-30 to 2025-10-4

## System Recovery & GitHub Reinitialisation**

**Focus:** System restoration, GitHub re-setup, and environment recovery after disk error.

**Context:**
Due to a macOS UI-level system error affecting the Macintosh HD volume (impacting multiple user accounts and safe mode functionality), I was required to **erase and reinstall macOS**. This process reset all local environments, Git, and VS Code configurations. It was unfortunate that it got to that point and I spent many hours trying to diagnose and then resolve the issue. 

**Actions Taken:**

* Backed up and reinstalled the system via macOS Recovery.
* Reinstalled **VS Code**, **Python**, and **Git**.
* Re-cloned the repository:
  `git clone ...
* Verified branch (`main`) and reconnected Git remote.
* Restored folder structure:

  ```
  maths/
  ├── evidence/
  Docs/
  algorithms/
  ```
* Confirmed Git identity and authentication.
* Re-added local study materials and ongoing notes.

**Outcome:**
System is now fully restored and version-controlled. All files synchronised from the GitHub remote repository.
Next focus: resume CS50 module progression and continue with discrete mathematics notes.

**Reflection:**
Although this was an unplanned interruption, the recovery process provided practical experience in **system reinitialisation**, **version control robustness**, and **environment reconfiguration** — useful foundational skills for future software development and systems engineering contexts.

## 2025-09-30
**Focus:** New software and websites, OH MY GIT, OSSU, Codedex, algoactionxyz. developer roadmaps. 

**Topics covered**
- OHMYGIT and agripongit
- Developer roadmaps
- OSSU
- Algorithm visualisers. 

**Work produced**
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-30/` (photos/scans)

**Time:** ~50 hours total (update)
EOF

# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-30

- **OHMYGIT and agripongit**: Getting used to git, notable commants here are git checkout HEAD. Go one back to get to new branch, generally reccomended to commit seperate files so you can get straight to issues rather than sort through seperately. 
- **Dev roadmaps**: Core Pathsways of: Game dev & server side. C++, systems design, data structures and algos,  rust. then supporting comp sci, python, AI engineer. 
- **OSSU**: Free online uni structure, syntactically valid statements, e.g cat god boy not valid by boy hugs cat is.  
- **Algroithm Visualisers**: Tried, csvistool, algo action and algorithm visualiser.org however i prefer most algo action and now its installed on phone. 


## 2025-09-28
**Focus:** Big O notation, Asymptotics, Scratch

**Topics covered**
- Asymptotic Complexity
- Log exercises
- Recurrences
- Recurrance traps

**Work produced**
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-28/` (photos/scans)

**Time:** ~47 hours total (update)
EOF

# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-28

- **Big-O upper bounds**: At worst, this grows like f(n) up to a constant, e.g., 3n^2 + 5n + 7 is O(n^2).
- **Big-O omega and theta**: “at least this fast”; Θ = “about this fast on both sides” (tight bound).Ignore constants & small terms: the highest-power term dominates (n^2 outruns n and constants).
- **Constants**: ne constant for all large n: when you claim O(n^2), the same bounding constant works for all n ≥ n0 (not step-to-step). 
- **Divide and Conquer**: Divide & conquer feel: halving the problem gives log n levels; ~n work per level ⇒ O(n log n)
- **Recurrences** T(n) = aT(n/b) + f(n); compare f(n) to n^(log_b a): smaller ⇒ Θ(n^(log_b a)); same×log^p ⇒ Θ(n^(log_b a)·log^(p+1)n); larger (with regularity) ⇒ Θ(f(n)).


## 2025-09-27
**Focus:** State Machines, Invariant principle.

**Topics covered**
- State machines
- Execution 
- Reachability
- Invariance

**Work produced**
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-27/` (photos/scans)

**Time:** ~44 hours total (update)
EOF

# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-27

- **State Machines**: M = (Q, q0, ->) with state set Q, start state q0 ∈ Q, and transition relation -> ⊆ Q×Q.
- **Excution**: A sequence q0, q1, …, qn with qi -> q(i+1) for all i.
- **Reachability**: q is reachable iff there exists an execution from q0 to q; Reach(M) is the least set containing q0 and closed under ->.  
- **Invariance**: Predicate I is invariant if it holds for all reachable states; prove with I(q0) and (I(p) ∧ p->q) ⇒ I(q).

## 2025-09-26
**Focus:** Diagonalisation, PageRank. 

**Topics covered**
- Eigenbasis example
- Page rank introduction
- Page rank lab 

**Work produced**
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)
- Code snipped referenced from Imperial LAB

**Time:** ~42 hours total (update)
EOF

# PageRank with damping 
# Minimal PageRank (power iteration)
import numpy as np

def pagerank(L, d=0.85, tol=1e-6, max_iter=1000):
    n = L.shape[0]
    J = np.ones((n, n)) / n
    M = d * L + (1 - d) * J
    r = np.ones(n) / n  # start uniform

    for _ in range(max_iter):
        r_next = M @ r
        if np.linalg.norm(r_next - r, 1) < tol:
            break
        r = r_next

    return 100 * r / r.sum()  # percentage style

# Example (4-node cycle):
# A→B→C→D→A
L = np.array([[0,0,0,1],
              [1,0,0,0],
              [0,1,0,0],
              [0,0,1,0]], dtype=float)

print(pagerank(L, d=0.85))


# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-26

- **PageRank introduction**: Loops, matrices, connections, dead ends, internat mapping
- **PageRank LAB**: Make sure to keep the code lines indented correctly, use n for number values. 
- **Module 5 review**: Diagonalisation, CD^nC^-1 =^n. λ^2 - (a+d)λ + (ad - bc) = 0, determinants, eigenbasis eigenvectors


## 2025-09-25
**Focus:** Proof by cases, Strong Induction. Harvard week 0.

**Topics covered**
- Proof By Cases
- Strong Induction
- Tautology
- Computer science foundations basic concepts. 

**Work produced**
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-25/` (photos/scans)

**Time:** ~38 hours total (update)
EOF

# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-25

- **Proof By Cases**: For any proposition C, the statement C or not C is a tautology, i.e., always true. So P is equivalent to True implies P, which is equivalent to (C or not C) implies P , which can be split into (C implies P ) and (not C implies P ). So to prove P, it’s enough to show that C implies P AND not C implies P. 'since S is true in both cases and these cases are exhaustive, S must be true.'
- **Strong Implication**: In a proof by induction, there are two parts: (1) the “base case”, which is the proof that P (0) holds, and (2) the “inductive step”, which is the proof that ∀n, P (n) =⇒ P (n + 1). Notice that in the inductive step, in order to prove P (n + 1) we may only assume the truth of P(n). The principle of strong induction says that this requirement can be relaxed:
- ## Proof techniques — quick notes
- **Existential proof (∃x P(x))** Goal: Show there exists an x with property P., Method:Construct a witness \(x^\*\) and prove \(P(x^\*)\).
- **Universal proof (∀x P(x))**Goal: Show every x has property P. Method: Let x be arbitrary, prove \(P(x)\) without using any special facts about x.
- **Implication by direct argument (P → Q)** Goal:* Prove “if P then Q”. Method: Assume P, logically derive Q.
- **Implication by contrapositive** Fact: \(P \rightarrow Q\) is equivalent to ¬Q → ¬P (not \(Q \rightarrow P\)). Method: Prove ¬Q ⇒ ¬P instead; often easier.
- **Proof by contradiction** Goal: Prove P. Method: Assume ¬P and derive a contradiction (False, or some \(R \land \lnot R\)). Hence P must be true.
- **Induction on ℕ (∀n∈ℕ P(n))** 1: Base case: prove \(P(0)\) (or \(P(1)\), depending on indexing). 2: Inductive step: assume \(P(k)\) (IH) and prove \(P(k+1)\).
- **CS50.ai**: Own personal ai we can use when on CS50. specific to the course. 

## 2025-09-24
**Focus:** Eigenvectors, Eigenbasis. Harvard week 0.

**Topics covered**
- What are eigenvalues and eigenvectors, with special eigen cases 
- Calculating Eigenvectors
- Changing to the Eigenbasis
- Computer science foundation basic concepts. 

**Work produced**
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-24/` (photos/scans)

**Time:** ~34 hours total (update)
EOF

# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-24

- **Eigenvectors vs Eigenvalues**: Eigen vectors are for if the vector stays in the same span, no matter if it flips 180. Eigenvalues are for the scale by how much the vector has changed, e.g if x1 its eigenvalue is 1, if x2 eigenvalue 2.  
- **Calculating Eigenvectors**: \χA​(λ)=λ2−(a+d)λ+(ad−bc)=0, Example: For A=[[3,4],[0,5]], characteristic polynomial: λ^2 - 8λ + 15; eigenvalues: 3 and 5.
- **Raising Matricies by Powers**: If all terms are zero except in the diagonal, when raising by powers its easy.  
- **Changing to the Eigenbasis**: If diagonalisable: T^{n} = C*D^{n}*C^{-1}.
- **Basic Computer science concepts**: bits bytes how to calculate. ASCII, Unicode. 


## 2025-09-23
**Focus:** Linear algebra for transformations + reflecting in a plane, Induction (theory + code)

**Topics covered**
- Reflecting In a Plane Example, using Gram-Schmidt Process
- Reflecting In a Plane Programming Assignment
- Proofs Discrete Mathematics, Induction workthroughs

**Work produced**
- Implemented Reflecting in a plane: (Code Below)
- Handwritten evidence planned in `maths/evidence/2025-09-23/` (photos)
- Written code of an induction proof

**Time:** ~30 hours total (updated)
EOF

# Reflecting In a Plane Code
cat > algorithms/PlaneReflection.py <<'EOF'
"""
Reflecting Bear (learning exercise).
Source: my practice solution inspired by Coursera/Imperial lab prompt.
"""

E  = gsBasis(bearBasis)          # 2x2 orthonormal columns
TE = np.array([[1., 0.],
               [0.,-1.]])        # reflect across first axis
T  = E @ TE @ E.T

# Induction Proof
\textbf{Claim.} For the sequence $x_{i+1}=6x_i-8x_{i-1}$ with $x_1=4$, $x_2=13$,
we have $x_i>0$ for all $i\ge 1$.

\textbf{Proof (strong induction with strengthened IH).}
Let $P(i)$ be: $(x_i>0)$ and $(x_i \ge 2x_{i-1}\text{ for }i\ge 2)$.

\emph{Base cases.} $x_1=4>0$. Also $x_2=13>0$ and $x_2\ge 2x_1$ since $13\ge 8$.

\emph{Inductive step.} Assume $P(k)$ holds for all $2\le k\le i$ (with $i\ge 2$).
Then $x_i>0$ and $x_i\ge 2x_{i-1}$, so $x_{i-1}\le \tfrac{1}{2}x_i$.
Hence
\[
x_{i+1}=6x_i-8x_{i-1}\ \ge\ 6x_i - 8\!\left(\tfrac{1}{2}x_i\right)
= 2x_i \ >\ 0.
\]
Thus $x_{i+1}>0$ and $x_{i+1}\ge 2x_i$, so $P(i+1)$ holds.

By strong induction, $x_i>0$ for all $i\ge 1$. \qed

# Uploading PDFs as updated folders onto github
Via Terminal
cd "/Users/estella/git-practice/imperial-app-prep/computing-application-prep-2026-imperial"
mkdir -p maths/evidence/2025-09-22 maths/evidence/2025-09-23

     # Making the dated evidence folder

for d in maths/evidence/2025-09-22 maths/evidence/2025-09-23; do
  { echo "# Evidence – ${d##*/}"; echo; 
    for f in "$d"/*.pdf; do [ -f "$f" ] && echo "- [$(basename "$f")](./$(basename "$f"))"; done; 
    echo; } > "$d/README.md"
done

     # After I drop PDFs into each folder, then auto-make folder indexes

git add -A
git commit -m "docs: log Day 8–9 and add evidence folders + indexes"
git push
 
     # Commit and push.

EOF

# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-23

- **Reflection in a plane**: \( r' = E * T_E * E^{-1} * r )
- **Proof by Induction**: Proof (we'll use), Base Case(more than 1), Inductive step (suppose), By the inductive process (proofs algebra), Completes inductive step (since LHS we have RHS)

EOF


EOF


## 2025-09-22
**Focus:** Linear algebra for transformations + orthogonality, plus Gram–Schmidt (theory + code)

**Topics covered**
- Einstein summation convention; symmetry of the dot product  
- Non-square matrix multiplication as applying a transform to many vectors  
- Projections via linear transforms (`r' = Ar`)  
- Changing basis & representing transforms in a new basis  
- Orthogonal matrices (`AᵀA = I`) & properties  
- Gram–Schmidt process (manual and coded)

**Work produced**
- Implemented Gram–Schmidt (fixed-size and general): `algorithms/gram_schmidt.py`
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-22/` (photos/scans)

**Time:** ~24 hours total (update)
EOF

# Gram–Schmidt code
cat > algorithms/gram_schmidt.py <<'EOF'
"""
Gram–Schmidt implementations (learning exercise).
Source: my practice solution inspired by Coursera/Imperial lab prompt.
"""

import numpy as np
import numpy.linalg as la

verySmallNumber = 1e-14

def gsBasis(A):
    B = np.array(A, dtype=np.float_)
    for i in range(B.shape[1]):
        for j in range(i):
            B[:, i] = B[:, i] - (B[:, i] @ B[:, j]) * B[:, j]
        if la.norm(B[:, i]) > verySmallNumber:
            B[:, i] = B[:, i] / la.norm(B[:, i])
        else:
            B[:, i] = np.zeros_like(B[:, i])
    return B
EOF

# Maths notes
cat > maths/notes.md <<'EOF'
# Maths Notes – 2025-09-22

- **Einstein summation**: repeated indices are summed (e.g., \( r'_i = A_{ij} r_j \)).
- **Projection via A**: \( r' = r - \hat{s}\, (r \cdot \hat{e}_3)/s_3 \) where \( s_3 = \hat{s}\cdot\hat{e}_3 \) (used for shadows).
- **Changing basis**: columns of \(A\) are the images of the old basis vectors.
- **Orthogonal matrices**: \( A^\top A = I \), preserve lengths/angles.
- **Gram–Schmidt**: subtract projections onto previous orthonormal vectors; normalize if nonzero.
EOF


