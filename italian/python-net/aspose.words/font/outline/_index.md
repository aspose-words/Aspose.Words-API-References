---
title: Font.outline property
linktitle: outline property
articleTitle: outline property
second_title: Aspose.Words for Python
description: "Font.outline property. True if the font is formatted as outline."
type: docs
weight: 300
url: /it/python-net/aspose.words/font/outline/
---

## Font.outline property

True if the font is formatted as outline.


```python
@property
def outline(self) -> bool:
    ...

@outline.setter
def outline(self, value: bool):
    ...

```

### Examples

Shows how to create a run of text formatted as outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Imposta la flag Outline per cambiare il colore di riempimento del testo a bianco e
# lascia un sottile contorno attorno a ogni carattere nel colore originale del testo.
builder.font.outline = True
builder.font.color = aspose.pydrawing.Color.blue
builder.font.size = 36
builder.writeln('This text has an outline.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Outline.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

