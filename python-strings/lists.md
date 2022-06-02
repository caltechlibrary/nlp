#### [3. Text Processing in Python](.)

## 3.3 Lists

A Python list is another iterable object. Like a string it is an ordered set of objects:

    a_list = [1, 2, 3, 1024]
    another_list = ['Once', 'upon', 'a', 'time', '...']

Lists do not have to be homogeneous:

    list3 = [1, 'Jack', 2, 'and the Beanstalk']
    list4 = [list3, another_list, a_list]

The output from `print(list4)` should look like this:

    [[1, 'Jack', 2, 'and the Beanstalk'], ['Once', 'upon', 'a', 'time', '...'], [1, 2, 3, 1024]]

Note that strings are enclosed in quotation marks, whereas variables (e.g. list3, list4) are not.

> **Exercise:** What output would you expect from this?

    for obj in list4:
      print(obj)

> **Exercise:** What output would you expect from this?

    for obj in list4:
      for subobj in obj:
        print(subobj)
        
> Try it out.

In NLP it is often useful to be able to change strings into lists and vice versa. The string methods `.split()`
and `.join()` make this easy. 

`string1.split(string2)` splits string1 at all incidents of string2 and puts the result into a list. If string2
is omitted that split will be on spaces.

For example:

    'Once upon a time ...'.split()

will return:

    ['Once', 'upon', 'a' 'time', '...']

But

    'Once upon a time ...'.split('e')

wil return:

    ['Onc', ' upon a tim', ' ...']

The `.join()` method does the opposite. `string2.join(list)` takes the elements in list and concatenates them
into a string with string 2 as a separator.

For instance:

    another_list = ['Once', 'upon', 'a', 'time', '...']
    ' '.join(another_list)

will return:

    'Once upon a time ...'

> **Exercise:** What does the following return:

    syllables = ['an', 'ti', 'di', 'ses', 'ta', 'blish', 'men', 'ta', 'ri', 'an', 'ism']
    ''.join(syllables)
    
    '
