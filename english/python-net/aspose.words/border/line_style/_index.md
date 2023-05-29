---
title: Border.line_style property
linktitle: line_style property
articleTitle: line_style property
second_title: Aspose.Words for Python
description: "Border.line_style property. Gets or sets the border style."
type: docs
weight: 40
url: /python-net/aspose.words/border/line_style/
---

## Border.line_style property

Gets or sets the border style.

If you set line style to none, then line width is automatically changed to zero.




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

