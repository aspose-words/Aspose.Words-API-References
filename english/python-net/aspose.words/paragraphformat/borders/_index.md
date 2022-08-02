---
title: borders property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets collection of borders of the paragraph."
type: docs
weight: 50
url: /python-net/aspose.words/paragraphformat/borders/
---

## ParagraphFormat.borders property

Gets collection of borders of the paragraph.


### Examples

Shows how to insert a paragraph with a top border.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

top_border = builder.paragraph_format.borders.top
top_border.color = drawing.Color.red
top_border.line_width = 4.0
top_border.line_style = aw.LineStyle.DASH_SMALL_GAP

builder.writeln("Text with a red top border.")

doc.save(ARTIFACTS_DIR + "Border.paragraph_top_border.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

