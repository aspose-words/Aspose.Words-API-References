---
title: underline_color property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the color of the underline applied to the font."
type: docs
weight: 540
url: /python-net/aspose.words/font/underline_color/
---

## Font.underline_color property

Gets or sets the color of the underline applied to the font.


### Examples

Shows how to configure the style and color of a text underline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.underline = aw.Underline.DOTTED
builder.font.underline_color = drawing.Color.red

builder.writeln("Underlined text.")

doc.save(ARTIFACTS_DIR + "Font.underlines.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

