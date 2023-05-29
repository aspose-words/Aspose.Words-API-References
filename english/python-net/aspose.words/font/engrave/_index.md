---
title: Font.engrave property
linktitle: engrave property
articleTitle: engrave property
second_title: Aspose.Words for Python
description: "Font.engrave property. True if the font is formatted as engraved."
type: docs
weight: 120
url: /python-net/aspose.words/font/engrave/
---

## Font.engrave property

True if the font is formatted as engraved.


### Examples

Shows how to apply engraving/embossing effects to text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.size = 36
builder.font.color = drawing.Color.light_blue

# Below are two ways of using shadows to apply a 3D-like effect to the text.
# 1 -  Engrave text to make it look like the letters are sunken into the page:
builder.font.engrave = True

builder.writeln("This text is engraved.")

# 2 -  Emboss text to make it look like the letters pop out of the page:
builder.font.engrave = False
builder.font.emboss = True

builder.writeln("This text is embossed.")

doc.save(ARTIFACTS_DIR + "Font.engrave_emboss.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

