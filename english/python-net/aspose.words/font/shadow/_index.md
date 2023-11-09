---
title: Font.shadow property
linktitle: shadow property
articleTitle: shadow property
second_title: Aspose.Words for Python
description: "Font.shadow property. True if the font is formatted as shadowed."
type: docs
weight: 330
url: /python-net/aspose.words/font/shadow/
---

## Font.shadow property

True if the font is formatted as shadowed.


```python
@property
def shadow(self) -> bool:
    ...

@shadow.setter
def shadow(self, value: bool):
    ...

```

### Examples

Shows how to create a run of text formatted with a shadow.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set the "shadow" flag to apply an offset shadow effect,
# making it look like the letters are floating above the page.
builder.font.shadow = True
builder.font.size = 36

builder.writeln("This text has a shadow.")

doc.save(ARTIFACTS_DIR + "Font.shadow.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

