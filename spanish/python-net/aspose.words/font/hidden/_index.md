---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /es/python-net/aspose.words/font/hidden/
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
# Con la bandera Hidden establecida en true, cualquier texto que creemos usando este objeto Font será invisible en el documento.
# No veremos ni resaltaremos texto oculto a menos que habilitemos la opción "Hidden text"
# se encuentra en Microsoft Word a través de "File" -> "Options" -> "Display". El texto seguirá allí,
# y podremos acceder a este texto programáticamente.
# No se recomienda usar este método para ocultar información sensible.
builder.font.hidden = True
builder.font.size = 36
builder.writeln('This text will not be visible in the document.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Hidden.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

