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
Lists are used to store multiple items in a single variable.    
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
If you want to create a list from series of numbers
```
n = 512

digits = list(str(n)))

print(digits) // [ '5', '1', '2']
```

### String Operations
https://repl.it/@webdevdave/Python-Basic-String-Operations#main.py

Length
```
my_string = "Hello World"
print(len(my_string)) // 11
```

Index
```
my_string = "Hello World"

print(my_string.index('e')) // 1
print(my_string.index('rld')) // a substring starting on index 8
```

Count occurences
```
my_string = "Hello World"

print(my_string.count('l')) // 3 times
```

Slice
```
my_string = "Hello World" 

print(my_string[:2])  // He
print(my_string[2:7]) // llo W
print(my_string[0:9:2]) //  every 2nd letter in slice HloWr
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

print(a == b) // True
print(a is b) // False because a and b take two different places in memory
```
### Loops
https://repl.it/@webdevdave/Python-Basic-Loops

for loop
```
def basic1(numbers):
    
    for i in numbers:
        print(i)
            
numbers = [1,2,3,4]
basic1(numbers)


def basic2(numbers):
    
    for index, val in enumerate(numbers):
        print(f"index{index} holds value {val}")
            
numbers = [1,2,3,4]
basic2(numbers)


def basic3(numbers):
    
    for i in range(len(numbers)):
        elem = numbers[i]
        print(f"index{i} holds element{elem}")
            
numbers = [1,2,3,4]
basic3(numbers)


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
https://repl.it/@webdevdave/Python-Basic-List-Comprehension#main.py
Words
```
sentence = "Every moment is a fresh beginning."
words = sentence.split()
word_lengths = []

for word in words:
  word_lengths.append(len(word))

print(word_lengths) // [5, 6, 2, 1, 5, 10]
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
### User Defined Functions
https://repl.it/@webdevdave/Python-Basic-User-Defined-Functions#main.py
Greeting
```
def greet(name, greeting):
  print("Hello %s %s" % (name, greeting))

greet('Tom Jones', "what's up?")
```

Double function
```
def double(x):
  return x * 2

print(double(5))
```
### User Defined Class
https://repl.it/@webdevdave/Python-Basic-User-Defined-Classes#main.py
```
class MyFirstClass:
    variable = "data"

    def function(self, number):
      print("I am in my function %d" % number)

a_class = MyFirstClass()
print(a_class.variable)
a_class.function(2)

b_class = MyFirstClass()
print(b_class.variable)
b_class.function(5)
```

### Dictionary Operations
https://repl.it/@webdevdave/Python-Basic-Dictionary-Operations#main.py    

Dictionaries are used to store data values in key:value pairs.    
A dictionary is a collection which is unordered, changeable and does not allow duplicates.    
```
phonebook = {
"Frank" : 121564789,
"Sarah" : 789456123,
"Kelly" : 456789133
}

print(phonebook)
```

```
print(phonebook["Frank"]) // 121564789
```

Iterating through a dictionary name is key & number is value.    
The items() method returns a view object. The view object contains the key-value pairs of the dictionary, as tuples in a list.
```
for name, number in phonebook.items():
  print("Name: %s,  Phone: %d" % (name, number))
```

Removing items from a dictionary
```
del phonebook["Frank"]
```
or POP can return the deleted value if print is used
```
phonebook.pop("Sarah")

print(phonebook)
```

Counting the number of vowels in a string 
- vowel_counts will be the dictionary holding the results.
- newStr was created b/c in python strings are immutable
- vowel_counts[vowel] is the key. count is the value
```
def get_count(input_str):
    vowel_counts = {}
    newStr = input_str

    for vowel in "aeiou":
        count = newStr.count(vowel)
        vowel_counts[vowel] = count

    print(vowel_counts)

get_count("there is a brown cow in the barn right now")
# {'a': 2, 'e': 3, 'i': 3, 'o': 3, 'u': 0}
```
Total count of vowels in a string

- In addition to what we have above, we create another 
variable to take in a list of the values (here list1).
- The print sums up the individual values of list1
```
def get_count(input_str):

    vowel_counts = {}
    newStr = input_str

    for vowel in "aeiou":
        count = newStr.count(vowel)
        vowel_counts[vowel] = count
        list1 = vowel_counts.values()

    print(sum(list1))

get_count("there is a brown cow in the barn right now")
# 11
```
