#### [Text Processing in Python](.)

## Strings and their properties

Here is an example of a string:

    'Peter Piper picked a peck of pickled peppers.'

Strings are designated by bounding single or double quotes.

This is a different string:

    '  Peter Piper picked a  peck of pickled peppers. '

The length property of a string is evaluated with the `len()` function:

    len('  Peter Piper picked a  peck of pickled peppers. ')

Note that the length includes the spaces. The `len()` function can be used to evaluate the length, or size, or
many different Python objects; not just text.

---
**Exercise:** Use the `len()` function to measure the length of the two strings above.

---

A 'function' is code that is independent of a specific object. A 'method' is code that is associated with an object. 
Use a period and the method name to access it, like this:

    'Peter Piper picked'.upper()

---
**Exercise:** 

Assign a string to a variable

     s = 'Peter Piper picked a peck of pickled peppers.'

What does the `upper()` method do? 

     s.upper()

Explore the following string methods:

     s.lower()
     
     s.title()
     
     s.count('p')
     
How often does 'p' appear in s? Count the occurences of 'pe'?

What does this do?

    s.lower().count('pe')

---
