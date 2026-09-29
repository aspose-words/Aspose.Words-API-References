---
title: Fill.preset_texture property
linktitle: preset_texture property
articleTitle: preset_texture property
second_title: Aspose.Words for Python
description: "Fill.preset_texture property. Gets a [PresetTexture](../../presettexture/) for the fill."
type: docs
weight: 170
url: /sv/python-net/aspose.words.drawing/fill/preset_texture/
---

## Fill.preset_texture property

Gets a [PresetTexture](../../presettexture/) for the fill.



```python
@property
def preset_texture(self) -> aspose.words.drawing.PresetTexture:
    ...

```

### Examples

Shows how to fill and tiling the texture inside the shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=80, height=80)
# Applicera texturjustering på formens fyllning.
shape.fill.preset_textured(aw.drawing.PresetTexture.CANVAS)
shape.fill.texture_alignment = aw.drawing.TextureAlignment.TOP_RIGHT
# Använd efterlevnadsalternativet för att definiera formen med DML om du vill få "TextureAlignment"
# egenskap efter att dokumentet sparas.
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

