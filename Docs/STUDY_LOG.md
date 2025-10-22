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
- 2
- 3

**Work produced**
- Code snippets below
- Notes added in `maths/notes.md`
- Handwritten evidence planned in `maths/evidence/2025-09-26/` (photos/scans)


**Time:** ~x hours total (updated)

- **DRY**: “Don't Repeat Yourself” (DRY) is a principle in software development aimed at reducing repetition and writing good clean code. Functions play a big part.
- **2**: text here


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