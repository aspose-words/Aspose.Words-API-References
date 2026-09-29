---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /it/python-net/aspose.words/font/hidden/
---

## Font.hidden property

True if the font is formatted as hidden text.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Examples

Shows how to create a run of hidden text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Con il flag Hidden impostato su true, qualsiasi testo che creiamo usando questo oggetto Font sarà invisibile nel documento.
# Non vedremo né evidenzieremo il testo nascosto a meno che non abilitiamo l'opzione "Hidden text"
# trovata in Microsoft Word tramite "File" -> "Options" -> "Display". Il testo sarà comunque presente,
# e potremo accedere a questo testo programmaticamente.
# Non è consigliato utilizzare questo metodo per nascondere informazioni sensibili.
builder.font.hidden = True
builder.font.size = 36
builder.writeln('This text will not be visible in the document.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Hidden.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

