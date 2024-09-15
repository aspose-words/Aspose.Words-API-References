---
title: TextureAlignment enumeration
linktitle: TextureAlignment enumeration
articleTitle: TextureAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.TextureAlignment enumeration. Specifies the alignment for the tiling of the texture fill."
type: docs
weight: 500
url: /python-net/aspose.words.drawing/texturealignment/
---

## TextureAlignment enumeration

Specifies the alignment for the tiling of the texture fill.


### Members

| Name | Description |
| --- | --- |
| TOP_LEFT | Top left texture alignment. |
| TOP | Top texture alignment. |
| TOP_RIGHT | Top right texture alignment. |
| LEFT | Left texture alignment. |
| CENTER | Center texture alignment. |
| RIGHT | Right texture alignment. |
| BOTTOM_LEFT | Bottom left texture alignment. |
| BOTTOM | Bottom texture alignment. |
| BOTTOM_RIGHT | Bottom right texture alignment. |
| NONE | None texture alignment. |

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

* module [aspose.words.drawing](../)

