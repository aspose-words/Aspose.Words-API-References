---
title: TextureAlignment enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the alignment for the tiling of the texture fill."
type: docs
weight: 420
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
builder = aw.DocumentBuilder(doc)

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 80, 80)

# Apply texture alignment to the shape fill.
shape.fill.preset_textured(aw.drawing.PresetTexture.CANVAS)
shape.fill.texture_alignment = aw.drawing.TextureAlignment.TOP_RIGHT

# Use the compliance option to define the shape using DML if you want to get "texture_alignment"
# property after the document saves.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT

doc.save(ARTIFACTS_DIR + "Shape.texture_fill.docx", save_options)
```

### See Also

* module [aspose.words.drawing](../)

