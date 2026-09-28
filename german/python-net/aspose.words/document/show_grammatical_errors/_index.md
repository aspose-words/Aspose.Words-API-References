---
title: Document.show_grammatical_errors property
linktitle: show_grammatical_errors property
articleTitle: show_grammatical_errors property
second_title: Aspose.Words for Python
description: "Document.show_grammatical_errors property. Specifies whether to display grammar errors in this document."
type: docs
weight: 420
url: /de/python-net/aspose.words/document/show_grammatical_errors/
---

## Document.show_grammatical_errors property

Specifies whether to display grammar errors in this document.


```python
@property
def show_grammatical_errors(self) -> bool:
    ...

@show_grammatical_errors.setter
def show_grammatical_errors(self, value: bool):
    ...

```

### Examples

Shows how to show/hide errors in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie zwei Sätze mit Fehlern ein, die erkannt werden würden
# durch die Rechtschreib- und Grammatikprüfungen in Microsoft Word.
builder.writeln('There is a speling error in this sentence.')
builder.writeln('Their is a grammatical error in this sentence.')
# Wenn diese Optionen aktiviert sind, werden Rechtschreibfehler unterstrichen
# im Ausgabedokument durch eine gezackte rote Linie, und eine doppelte blaue Linie hebt grammatikalische Fehler hervor.
doc.show_grammatical_errors = show_errors
doc.show_spelling_errors = show_errors
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingAndGrammarErrors.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

