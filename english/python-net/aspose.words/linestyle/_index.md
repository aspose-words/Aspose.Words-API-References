---
title: LineStyle enumeration
linktitle: LineStyle enumeration
articleTitle: LineStyle enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LineStyle enumeration. Specifies line style of a [Border](../border/)."
type: docs
weight: 650
url: /python-net/aspose.words/linestyle/
---

## LineStyle enumeration

Specifies line style of a [Border](../border/).



### Members

| Name | Description |
| --- | --- |
| NONE |  |
| SINGLE |  |
| THICK |  |
| DOUBLE |  |
| HAIRLINE |  |
| DOT |  |
| DASH_LARGE_GAP |  |
| DOT_DASH |  |
| DOT_DOT_DASH |  |
| TRIPLE |  |
| THIN_THICK_SMALL_GAP |  |
| THICK_THIN_SMALL_GAP |  |
| THIN_THICK_THIN_SMALL_GAP |  |
| THIN_THICK_MEDIUM_GAP |  |
| THICK_THIN_MEDIUM_GAP |  |
| THIN_THICK_THIN_MEDIUM_GAP |  |
| THIN_THICK_LARGE_GAP |  |
| THICK_THIN_LARGE_GAP |  |
| THIN_THICK_THIN_LARGE_GAP |  |
| WAVE |  |
| DOUBLE_WAVE |  |
| DASH_SMALL_GAP |  |
| DASH_DOT_STROKER |  |
| EMBOSS_3D |  |
| ENGRAVE_3D |  |
| OUTSET |  |
| INSET |  |

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

* module [aspose.words](../)

