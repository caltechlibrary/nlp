## 3. spaCy

- 3.1 [Introduction to spaCy](#spacy)
- 3.1 [Processing pipelines](#pipe)
- 3.2 [Text modelling](#model)
- 3.3 [Word vectors and similarity](#vec)
- 3.4 [spaCy examples](#ex)

### <a name='spacy'/>3.1 Introduction to spacy

spaCy is an open source Python library for Natural Language Processing with a focus on rapid development 
and production usage. Here is an example of spaCy code to extract 'entities' from a text:

```python
import spacy  # import the spaCy library
nlp = spacy.load('en_core_web_sm')  # load the processing pipeline, `nlp`, based on the 'en_core_web_sm' model
text = '''
  Founded in 1891, Caltech is a world-renowned
  science and engineering institute that marshals
  some of the world’s brightest minds and most
  innovative tools to address fundamental scientific
  questions and pressing societal challenges. An
  independent, privately supported institution
  located in Pasadena, California, Caltech also
  manages the Jet Propulsion Laboratory (JPL),
  located 6 miles north of campus, for NASA.'''
doc = nlp(text)  # create an nlp object named `doc` from the text using the model
for ent in doc.ents:  # read the 'entities', and their labels, from `doc`
  print(ent.text, ent.label_)
```
(GPE = stands for 'Geopolitical entity')




### <a name='pipe'/>3.1 Processing pipelines

### <a name='model'/>3.2 Statistical modelling of text

### <a name='vec'/>3.3 Acquiring a text

### <a name='ex'/>3.4 Acquiring a text


---

##### \< [2. NLTK](nltk.md) \| [4. Resources](resources.md) \>

