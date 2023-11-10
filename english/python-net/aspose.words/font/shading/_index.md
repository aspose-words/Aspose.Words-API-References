---
title: Font.shading property
linktitle: shading property
articleTitle: shading property
second_title: Aspose.Words for Python
description: "Font.shading property. Returns a [Shading](../../shading/) object that refers to the shading formatting for the font."
type: docs
weight: 320
url: /python-net/aspose.words/font/shading/
---

## Font.shading property

Returns a [Shading](../../shading/) object that refers to the shading formatting for the font.



```python
@property
def shading(self) -> aspose.words.Shading:
    ...

```

### Examples

Shows how to apply shading to text created by a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.color = drawing.Color.white

# One way to make the text created using our white font color visible
# is to apply a background shading effect.
shading = builder.font.shading
shading.texture = aw.TextureIndex.TEXTURE_DIAGONAL_UP
shading.background_pattern_color = drawing.Color.orange_red
shading.foreground_pattern_color = drawing.Color.dark_blue

builder.writeln("White text on an orange background with a two-tone texture.")

doc.save(ARTIFACTS_DIR + "Font.shading.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

