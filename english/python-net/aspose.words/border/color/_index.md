---
title: Border.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "Border.color property. Gets or sets the border color."
type: docs
weight: 10
url: /python-net/aspose.words/border/color/
---

## Border.color property

Gets or sets the border color.


```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

@color.setter
def color(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to insert a string surrounded by a border into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.border.color = drawing.Color.green
builder.font.border.line_width = 2.5
builder.font.border.line_style = aw.LineStyle.DASH_DOT_STROKER

builder.write("Text surrounded by green border.")

doc.save(ARTIFACTS_DIR + "Border.font_border.docx")
```

### See Also

* module [aspose.words](../../)
* class [Border](../)

