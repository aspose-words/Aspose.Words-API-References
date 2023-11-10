---
title: Border.line_width property
linktitle: line_width property
articleTitle: line_width property
second_title: Aspose.Words for Python
description: "Border.line_width property. Gets or sets the border width in points."
type: docs
weight: 50
url: /python-net/aspose.words/border/line_width/
---

## Border.line_width property

Gets or sets the border width in points.


```python
@property
def line_width(self) -> float:
    ...

@line_width.setter
def line_width(self, value: float):
    ...

```

### Remarks

If you set line width greater than zero when line style is none, the line style is
automatically changed to single line.




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

