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
