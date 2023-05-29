---
title: Font.outline property
linktitle: outline property
articleTitle: outline property
second_title: Aspose.Words for Python
description: "Font.outline property. True if the font is formatted as outline."
type: docs
weight: 290
url: /python-net/aspose.words/font/outline/
---

## Font.outline property

True if the font is formatted as outline.


### Examples

Shows how to create a run of text formatted as outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set the "outline" flag to change the text's fill color to white and
# leave a thin outline around each character in the original color of the text.
builder.font.outline = True
builder.font.color = drawing.Color.blue
builder.font.size = 36

builder.writeln("This text has an outline.")

doc.save(ARTIFACTS_DIR + "Font.outline.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

