---
title: Font.line_spacing property
linktitle: line_spacing property
articleTitle: line_spacing property
second_title: Aspose.Words for Python
description: "Font.line_spacing property. Returns line spacing of this font (in points)."
type: docs
weight: 190
url: /python-net/aspose.words/font/line_spacing/
---

## Font.line_spacing property

Returns line spacing of this font (in points).


```python
@property
def line_spacing(self) -> float:
    ...

```

### Examples

Shows how to get a font's line spacing, in points.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Set different fonts for the DocumentBuilder and verify their line spacing.
builder.font.name = 'Calibri'
self.assertEqual(14.6484375, builder.font.line_spacing)
builder.font.name = 'Times New Roman'
self.assertEqual(13.798828125, builder.font.line_spacing)
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

