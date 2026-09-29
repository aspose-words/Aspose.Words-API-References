---
title: Font.no_proofing property
linktitle: no_proofing property
articleTitle: no_proofing property
second_title: Aspose.Words for Python
description: "Font.no_proofing property. True when the formatted characters are not to be spell checked."
type: docs
weight: 280
url: /it/python-net/aspose.words/font/no_proofing/
---

## Font.no_proofing property

True when the formatted characters are not to be spell checked.


```python
@property
def no_proofing(self) -> bool:
    ...

@no_proofing.setter
def no_proofing(self, value: bool):
    ...

```

### Examples

Shows how to prevent text from being spell checked by Microsoft Word.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Normalmente, Microsoft Word evidenzia gli errori ortografici con una sottolineatura rossa irregolare.
# Possiamo rimuovere la flag "NoProofing" per creare una porzione di testo che
# ignora il correttore ortografico disattivandolo completamente.
builder.font.no_proofing = True
builder.writeln('Proofing has been disabled, so these spelking errrs will not display red lines underneath.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NoProofing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

