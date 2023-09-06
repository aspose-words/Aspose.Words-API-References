---
title: ParagraphFormat.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for Python
description: "ParagraphFormat.borders property. Gets collection of borders of the paragraph."
type: docs
weight: 60
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
top_border.line_width = 4.0
top_border.line_style = aw.LineStyle.DASH_SMALL_GAP
# Set ThemeColor only when LineWidth or LineStyle setted.
top_border.theme_color = awthemes.ThemeColor.ACCENT1
top_border.tint_and_shade = 0.25

builder.writeln("Text with a top border.")

doc.save(ARTIFACTS_DIR + "Border.paragraph_top_border.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

