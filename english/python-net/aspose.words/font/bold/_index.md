---
title: bold property
second_title: Aspose.Words for Python via .NET API Reference
description: "True if the font is formatted as bold."
type: docs
weight: 40
url: /python-net/aspose.words/font/bold/
---

## Font.bold property

True if the font is formatted as bold.


### Examples

Shows how to insert formatted text using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Specify font formatting, then add text.
font = builder.font
font.size = 16
font.bold = True
font.color = drawing.Color.blue
font.name = "Courier New"
font.underline = aw.Underline.DASH

builder.write("Hello world!")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

