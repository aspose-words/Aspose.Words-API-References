---
title: Font.spacing property
linktitle: spacing property
articleTitle: spacing property
second_title: Aspose.Words for Python
description: "Font.spacing property. Returns or sets the spacing (in points) between characters ."
type: docs
weight: 390
url: /it/python-net/aspose.words/font/spacing/
---

## Font.spacing property

Returns or sets the spacing (in points) between characters .


```python
@property
def spacing(self) -> float:
    ...

@spacing.setter
def spacing(self, value: float):
    ...

```

### Examples

Shows how to set horizontal scaling and spacing for characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Aggiungi un run di testo e aumenta la larghezza dei caratteri al 150%.
builder.font.scaling = 150
builder.writeln('Wide characters')
# Aggiungi un run di testo e aggiungi 1 pt di spaziatura orizzontale extra tra ogni carattere.
builder.font.spacing = 1
builder.writeln('Expanded by 1pt')
# Aggiungi un run di testo e avvicina i caratteri di 1 pt.
builder.font.spacing = -1
builder.writeln('Condensed by 1pt')
doc.save(file_name=ARTIFACTS_DIR + 'Font.ScalingSpacing.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

