## 3. spaCy

- 3.1 [Introduction to spaCy](#spacy)
- 3.2 [Processing pipelines](#pipe)
- 3.3 [Text modelling](#model)
- 3.4 [Word vectors and similarity](#vec)
- 3.5 [spaCy examples](#ex)

### <a name='spacy'/>3.1 Introduction to spacy

spaCy is an open source Python library for Natural Language Processing with a focus on rapid development 
and production usage. Here is an example of spaCy code to extract 'entities' from a text:

```python
import spacy                        # import the spaCy library
nlp = spacy.load('en_core_web_sm')  # load the processing pipeline
text = ("Founded in 1891, Caltech is an "
        "independent, privately supported institution "
        "located in Pasadena, California. Caltech also "
        "manages the Jet Propulsion Laboratory (JPL), "
        "located 6 miles north of campus, for NASA.")
doc = nlp(text)                     # create an nlp object named `doc`
for ent in doc.ents:                # read the 'entities' and their labels, from `doc`
  print(ent.text, ent.label_)
```
##### (GPE = 'Geopolitical entity')

In its most basic form a spaCy application can be very short, but a lot of processing steps take place,
and a lot more information is contained within the `doc` object.

### <a name='pipe'/>3.2 Processing pipelines

We can list the contents of the processing pipeline with:

```python
print(nlp.pipe_names)
```

This will list the default pipeline components, in the order in which they are used:

| tok2vec | Assign token-to-vector embeddings |
| tagger | Assign part-of-speech-tags |
| parser | Assign dependency labels |
| attribute_ruler | Assign token attribute mappings and rule-based exceptions |
| lemmatizer | Assign base forms to words using rules and lookups |
| ner | Assign named entities |

##### (from: [https://spacy.io/usage/processing-pipelines#pipelines](https://spacy.io/usage/processing-pipelines#pipelines)

If your result is a shorter list of pipeline components then you are likely not using the most recent version of spaCy.

Here is some of the information that is available from the `nlp` object:

```python
import pandas as pd
attribs = []
for token in doc:
  attribs.append([token.text, token.lemma_, token.pos_, token.tag_, token.dep_,
            token.shape_, token.is_alpha, token.is_stop])
df = pd.DataFrame(attribs, columns=['text', 'lemma', 'POS', 'tag', 'dependency', 'shape', 'alpha', 'stop'])
df
```

##### (There is a full list of token attributes here: [https://spacy.io/api/token#attributes](https://spacy.io/api/token#attributes))

### <a name='model'/>3.3 Text modelling

### <a name='vec'/>3.4 Word vectors and similarity

Similarity

import spacy

nlp = spacy.load("en_core_web_md")  # make sure to use larger package!
doc1 = nlp("I like salty fries and hamburgers.")
doc2 = nlp("Fast food tastes very good.")

Similarity of two documents
print(doc1, "<->", doc2, doc1.similarity(doc2))
Similarity of tokens and spans
french_fries = doc1[2:4]
burgers = doc1[5]
print(french_fries, "<->", burgers, french_fries.similarity(burgers))

### <a name='ex'/>3.5 spaCy examples

---

##### \< [2. NLTK](nltk.md) \| [4. Resources](resources.md) \>

