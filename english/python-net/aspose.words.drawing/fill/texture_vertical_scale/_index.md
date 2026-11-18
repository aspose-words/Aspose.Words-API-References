---
title: Fill.texture_vertical_scale property
linktitle: texture_vertical_scale property
articleTitle: texture_vertical_scale property
second_title: Aspose.Words for Python
description: "Fill.texture_vertical_scale property. Gets or sets the vertical scale for tile texture fill."
type: docs
weight: 5703
url: /python-net/aspose.words.drawing/fill/texture_vertical_scale/
---

## Fill.texture_vertical_scale property

Gets or sets the vertical scale for tile texture fill.


```python
@property
def texture_vertical_scale(self) -> float:
    ...

@texture_vertical_scale.setter
def texture_vertical_scale(self, value: float):
    ...

```

### Examples

Shows how to scale a tiled texture fill of a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=200, height=200)
shape.fill.preset_textured(aw.drawing.PresetTexture.CANVAS)
fill = shape.fill
# Check whether the shape's fill is a tiled texture before scaling it.
if fill.texture_tile:
# A scale of 1 is equivalent to 100%. Values can exceed 100%.
    fill.texture_horizontal_scale = 0.5
    fill.texture_vertical_scale = 2.15
# Use the compliance option to define the shape using DML
# to keep the texture scale properties after the document saves.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
doc.save(file_name=ARTIFACTS_DIR + "Shape.TextureTile.docx", save_options=save_options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

