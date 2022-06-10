## 2. NLTK

- 2.1 [Acquiring a text](#acq)
- 2.2 [Text preprocessing](#preprocessing)
- 2.3 [Word contexts and frequency distribution](#freq)
- 2.4 [Parts-of-speech tagging](#pos)
- 2.5 [Named entity recognition](#ner)
- 2.6 [Sentiment analysis](#sa)

### <a name='acq'/>2.1 Acquiring a text

There are many different ways to acquire a text for processing. The text may already be in text form, 
in a file stored on your computer. Or an HTML-encoded file on the web. Or an audio or video file. 
Or a scan of a handwritten image. There are increasingly sophisticated and successful ways for recognizing 
and transcribing texts from images, audio, and video formats, and we will assume that that type of 
processing has already taken place.

Here is code for storing a file locally:

    # assign a text to a variable, `title`
    title = 'A Town Called Alice'
    
    # open a file for writing, assign to variable `f`
    with open('demofile.txt', 'w') as f:
      f.write(title)
      
    # open a file for appending, assign to variable `f`
    with open('demofile.txt', 'a') as f:
      f.write(', by Nevil Shute')
      
    # open a file file reading, assign to variable `f`
    with open('demofile.txt', 'r') as f:
      title2 = f.read()
      
    print('Title:', title)
    print('Title with author:', title2)
    
Note the attributes 'w', 'a' and 'r' for 'write' (i.e. overwrite, create), 'append', and 'read' on the open function.
Also, the file is automatically closed at the end of each `open()` code block.

For reading text from the web we will use the `request` method from the `urllib` library to download the text of 'Origin of the Species'
from [Project Gutenberg](https://www.gutenberg.org/). We will use this version: [The Origin of Species by Means of Natural Selection by Charles Darwin (6th. ed.)](https://www.gutenberg.org/ebooks/2009)

### <a name='preprocessing'/>2. Text preprocessing

### <a name='freq'/>2.- 2.3 Word contexts and frequency distribution

### <a name='pos'/>2.- 2.4 Parts-of-speech tagging

### <a name='ner'/>2.- 2.5 Named entity recognition

### <a name='sa'/>2.- 2.6 Sentiment analysis

---

##### \< [1. Text Processing in Python](python-strings.md) \| [3. spaCy](spacy.md) \>

