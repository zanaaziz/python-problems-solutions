# Some Python Problems and Solutions
This repo is just a collection of some sample problems in Python and how I'd go about solving them.

Nothing revolutionary by any means.

Just messing about with Python.

# Words of a String Starting With a Certain Letter
```python
st = "This is a sample sentence that is trying it's best to extend itself."
for word in st.lower().split():
    if word[0] == "t":
        print(word)
```

# Counting The Letters In a Word Within a String
```python
st = 'Print every word in this sentence that has an even number of letters'
for word in st.split():
    if len(word) % 2 == 0:
        print(word)
    else:
        pass
```

# Creating a List of The First Letters of Every Word In a String
```python
st = 'This should get the first letter of every word in this string.'
first_letters = [c[0] for c in st.split()]
print(first_letters)
```

# Iterating Through a Range & Checking For a Certain Type of Number
```python
for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        print(i, "FizzBuzz")
    elif i % 3 == 0:
        print(i, "Fizz")
    elif i % 5 == 0:
        print(i, "Buzz")
    else:
        pass
```

# Removing Multiple Characters From a String
```python
text = "“The brown fox jumped over the rain deer because he felt like it.”"

for c in ['“', '”']:
    if c in text:
        text = text.replace(c, "")
```

**Here we are checking if the number is a multiple of 3 and 5.**

# Getting The First Letter of Every Word In a String
```python
st = 'Create a list of the first letters of every word in this string'
first_letters = [c[0] for c in st.split()]
print(first_letters)
```

# Getting Uppercase & Lowercase Words In a String
```python
def up_low(s):
    upper_words = [word for word in s.split() if word[0].isupper()]
    print("\nUppercase Words: ", len(upper_words))

    lower_words = [word for word in s.split() if word[0].islower()]
    print("\nLowercase Words: ", len(lower_words))

up_low("This is Zana's string in Python.")
```

# Modifying Elements Within a List
```python
def multiply(l):
    total = 1

    for e in l:
        total *= e

    return total

print(multiply([2, 2, 2]))
```

**Here we are multiplying all the elements by each other.**

# Checking For a Palindrome In a String
```python
def palindrome(s):
    s = s.replace(" ","")
    return s == s[::-1]

print(palindrome("bob"))
```

**A palindrome is a word that reads the same way backwards.**

# Checking For a Pangram In a String
```python
import string
def ispangram(s, alphabet=string.ascii_lowercase):
    alphaset = set(alphabet)

    return alphaset <= set(s.lower())

print(ispangram("The quick brown fox jumps over the lazy dog"))
```

**A pangram is a sentence that contains all the letters of the alphabet at least once.**
