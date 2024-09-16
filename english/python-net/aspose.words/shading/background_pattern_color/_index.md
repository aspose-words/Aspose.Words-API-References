---
title: Shading.background_pattern_color property
linktitle: background_pattern_color property
articleTitle: background_pattern_color property
second_title: Aspose.Words for Python
description: "Shading.background_pattern_color property. Gets or sets the color that's applied to the background of the [Shading](../) object."
type: docs
weight: 10
url: /python-net/aspose.words/shading/background_pattern_color/
---

## Shading.background_pattern_color property

Gets or sets the color that's applied to the background of the [Shading](../) object.



```python
@property
def background_pattern_color(self) -> aspose.pydrawing.Color:
    ...

@background_pattern_color.setter
def background_pattern_color(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to decorate text with borders and shading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
borders = builder.paragraph_format.borders
borders.distance_from_text = 20
borders.get_by_border_type(aw.BorderType.LEFT).line_style = aw.LineStyle.DOUBLE
borders.get_by_border_type(aw.BorderType.RIGHT).line_style = aw.LineStyle.DOUBLE
borders.get_by_border_type(aw.BorderType.TOP).line_style = aw.LineStyle.DOUBLE
borders.get_by_border_type(aw.BorderType.BOTTOM).line_style = aw.LineStyle.DOUBLE
shading = builder.paragraph_format.shading
shading.texture = aw.TextureIndex.TEXTURE_DIAGONAL_CROSS
shading.background_pattern_color = aspose.pydrawing.Color.light_coral
shading.foreground_pattern_color = aspose.pydrawing.Color.light_salmon
builder.write('This paragraph is formatted with a double border and shading.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.ApplyBordersAndShading.docx')
```

### See Also

* module [aspose.words](../../)
* class [Shading](../)

