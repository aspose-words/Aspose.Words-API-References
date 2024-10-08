﻿---
title: Fill.texture_alignment property
linktitle: texture_alignment property
articleTitle: texture_alignment property
second_title: Aspose.Words for Python
description: "Fill.texture_alignment property. Gets or sets the alignment for tile texture fill."
type: docs
weight: 190
url: /python-net/aspose.words.drawing/fill/texture_alignment/
---

## Fill.texture_alignment property

Gets or sets the alignment for tile texture fill.


```python
@property
def texture_alignment(self) -> aspose.words.drawing.TextureAlignment:
    ...

@texture_alignment.setter
def texture_alignment(self, value: aspose.words.drawing.TextureAlignment):
    ...

```

### Examples

Shows how to fill and tiling the texture inside the shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Apply texture alignment to the shape fill.
shape.fill.preset_textured(aw.drawing.PresetTexture.CANVAS)
shape.fill.texture_alignment = aw.drawing.TextureAlignment.TOP_RIGHT
# Use the compliance option to define the shape using DML if you want to get "TextureAlignment"
# property after the document saves.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextureFill.docx', save_options=save_options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.TextureFill.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual(aw.drawing.TextureAlignment.TOP_RIGHT, shape.fill.texture_alignment)
self.assertEqual(aw.drawing.PresetTexture.CANVAS, shape.fill.preset_texture)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

