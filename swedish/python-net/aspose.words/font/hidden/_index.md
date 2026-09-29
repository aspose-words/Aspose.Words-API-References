---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /sv/python-net/aspose.words/font/hidden/
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
# När flaggan Hidden är satt till true kommer all text som vi skapar med detta Font-objekt att vara osynlig i dokumentet.
# Vi kommer inte att se eller markera dold text om vi inte aktiverar alternativet "Hidden text"
# finns i Microsoft Word via "File" -> "Options" -> "Display". Texten kommer fortfarande att finnas där,
# och vi kommer att kunna komma åt denna text programmässigt.
# Det rekommenderas inte att använda denna metod för att dölja känslig information.
builder.font.hidden = True
builder.font.size = 36
builder.writeln('This text will not be visible in the document.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.Hidden.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

