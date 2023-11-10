---
title: Font.italic property
linktitle: italic property
articleTitle: italic property
second_title: Aspose.Words for Python
description: "Font.italic property. True if the font is formatted as italic."
type: docs
weight: 160
url: /python-net/aspose.words/font/italic/
---

## Font.italic property

True if the font is formatted as italic.


```python
@property
def italic(self) -> bool:
    ...

@italic.setter
def italic(self, value: bool):
    ...

```

### Examples

Shows how to write italicized text using a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.size = 36
builder.font.italic = True
builder.writeln("Hello world!")

doc.save(ARTIFACTS_DIR + "Font.italic.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

