# Python Basics
The basics to get started

### Print
https://repl.it/@webdevdave/Python-Basic-Print

The most common use
```
print("Cookie Monster")
```

Using the format string method
```
x = 12345
y = 'Kelly'

print('{}, and {}' .format(x, y))
```

Using the f-string, not to be confused with the f-bomb
```
x = 4567
y = 'Cookie monster'
print(f'x is {x} and y is {y}')
```

Old school - %d is for data, %s is for string
```
x = 9594934
y = 'Oingo Boingo'
print('%d and %s', %(x, y))
```

### Basic Types
https://repl.it/@webdevdave/Python-Basic-Types#main.py

Integer
```
my_int = 3
my_int int(3) # typecasting
```
Float
```
my_float = 3.2
my_float = float(3.2) # typecasting
```
String
```
my_string = "Humpty Dumpty"
my_string = str(5) # making an int a string
print(type(my_string))
```

### Basic List
https://repl.it/@webdevdave/Python-Basic-List#main.py
Similar to arrays

Declare a list
```
my_list = [1,2,3,4,5]
```
Access List
```
my_list = [1,2,3,4,5]
print(my_list[0])
```
Add values
```
my_list[1,2,3]
my_list.append(4)
print(my_list)
```

### String Operations
https://repl.it/@webdevdave/Python-Basic-String-Operations#main.py

Length
```
my_string = "Hello World"
print(len(my_string))
```

Index
```
print(my_string.index('e'))
print(my_string.index('rld')) # substring
```

Count occurences
```
print(my_string.count('l')) # 3 times
```

Slice
```
print(my_string[:2])
print(my_string[2:7])
print(my_string[2:9:2]) # every 2nd letter in slice
```

Reverse
```
print(my_string[::-1])
```

Upper case
```
print(my_string.upper())
```
Lower case
```
print(my_string.lower())
```

Starts with
```
print(my_string.startswith("P"))
print(my_string.startswith("H"))
print(my_string.startswith("Hello"))
```

Ends with
```
print(my_string.endswith("d"))
print(my_string.endswith("World"))
```

Split string
```
print(my_string.split(" ")) # puts into a list
print(my_string.split(", ")) # puts into list w/o comma
```

### Conditionals and Booleans
https://repl.it/@webdevdave/Python-Basic-Boolean#main.py

use comparison operators
```
x = 10
print(x == 10)
print(x > 11)
```

use and + or
```
name = "Kelly"
age = 30

if name == "Kelly" and age == 30:
  print("Yes, it's true")

if name == "Kelly" or age == 35:
  print("Got one of them right")
```

use in
```
years = [2015, 2016, 2017, 2018, 2019, 2020]
year = 2015

if year in years:
  print("yes")
```

use == vs is
```
a = [1,2,3]
b = [1,2,3]

print(a == b)
print(a is b) # two different places in memory

use not
print(not True)
```
### Loops

for loop
```
for x in range(5):
  print(x)
 
print('\n') # separate outputs

for x in range(1, 11):
  print(x) # print values from 1 to 10

print('\n') # separate outputs

for x in range(1, 11, 2):
    print(x) # every second value

print('\n') # separate outputs
```

while
```
x = 0
while x < 5:
  print('x', x)
  x += 1

print('\n') # separate outputs
y = 0
while True:
  if y == 5:
    break
  print('y', y)
  y += 1

print('\n') # separate outputs

z = 0
while z < 10:
  z += 1
  if z % 2 == 0:
    # endless loop if z += 1 here
    continue
  print('z', z)
  ```
  
### List Comprehension
Words
```
sentence = "Every moment is a fresh beginning."
words = sentence.split()
word_lengths = []

for word in words:
  word_lengths.append(len(word))

print(word_lengths)
```

list comprehension     
find the lengh of the word for word in words     
```
word_lengths = [len(word) for word in words]
print(word_lengths)
```

Numbers
```
numbers = [1,2,3,4,5,6,7,8,9,10]
even_number = []

for number in numbers:
  if number % 2 == 0:
    even_number.append(number)
print(even_number)
```

list comprehension
```
even_number2 = [number for number in numbers if number % 2 == 0]
print(even_number)
```
