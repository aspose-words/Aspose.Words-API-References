---
title: FindReplaceOptions.find_whole_words_only property
linktitle: find_whole_words_only property
articleTitle: find_whole_words_only property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.find_whole_words_only property. True indicates the oldValue must be a standalone word."
type: docs
weight: 50
url: /fr/python-net/aspose.words.replacing/findreplaceoptions/find_whole_words_only/
---

## FindReplaceOptions.find_whole_words_only property

True indicates the oldValue must be a standalone word.


```python
@property
def find_whole_words_only(self) -> bool:
    ...

@find_whole_words_only.setter
def find_whole_words_only(self, value: bool):
    ...

```

### Examples

Shows how to toggle standalone word-only find-and-replace operations.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Jackson will meet you in Jacksonville.')
# Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
options = aw.replacing.FindReplaceOptions()
# Définir le drapeau "FindWholeWordsOnly" sur "true" pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
# Définir le drapeau "FindWholeWordsOnly" sur "false" pour remplacer tout le texte, quel que soit son contexte.
options.find_whole_words_only = find_whole_words_only
doc.range.replace(pattern='Jackson', replacement='Louis', options=options)
self.assertEqual('Louis will meet you in Jacksonville.' if find_whole_words_only else 'Louis will meet you in Louisville.', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

