﻿---
title: Font.emboss property
linktitle: emboss property
articleTitle: emboss property
second_title: Aspose.Words for Python
description: "Font.emboss property. True if the font is formatted as embossed."
type: docs
weight: 100
url: /python-net/aspose.words/font/emboss/
---

## Font.emboss property

True if the font is formatted as embossed.


```python
@property
def emboss(self) -> bool:
    ...

@emboss.setter
def emboss(self, value: bool):
    ...

```

### Examples

Shows how to apply engraving/embossing effects to text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.size = 36
builder.font.color = aspose.pydrawing.Color.light_blue
# Below are two ways of using shadows to apply a 3D-like effect to the text.
# 1 -  Engrave text to make it look like the letters are sunken into the page:
builder.font.engrave = True
builder.writeln('This text is engraved.')
# 2 -  Emboss text to make it look like the letters pop out of the page:
builder.font.engrave = False
builder.font.emboss = True
builder.writeln('This text is embossed.')
doc.save(file_name=ARTIFACTS_DIR + 'Font.EngraveEmboss.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

