#### [3. Text Processing in Python](.)

## 3.2 Strings as Iterables

A string is an ordered set of symbols: letters, numbers, and other characters.
The position of each symbol can be ascertained with with .index() method. The following will
return the position of 't' in the string. Note that the first position is '0', not '1'.
This is known as 'zero-based' indexing.

    opening = 'Once upon a time...'
    print(opening.index('t'))
    
An object that consist of an ordered set of other objects is 'iterable', because you can iterate,
or loop over those objects. A string consists of an ordered set of single-characters strings, so
it is iterable. That is, 'Once upon a time...' consists of 'O', 'n', 'c', 'e', etc. The indexes of
the characters are 0, 1, 2, 3, 4, etc.

Iterable objects can be looped over like this:

    for character in opening:
        print(character)

> **Exercise:** Can you explain the output for the following:

    for character in opening:
        print(opening.index(character))

