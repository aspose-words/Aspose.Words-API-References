---
title: ParagraphFormat.shading property
linktitle: shading property
articleTitle: shading property
second_title: Aspose.Words for Python
description: "ParagraphFormat.shading property. Returns a [Shading](../../shading/) object that refers to the shading formatting for the paragraph."
type: docs
weight: 290
url: /python-net/aspose.words/paragraphformat/shading/
---

## ParagraphFormat.shading property

Returns a [Shading](../../shading/) object that refers to the shading formatting for the paragraph.



```python
@property
def shading(self) -> aspose.words.Shading:
    ...

```

### Examples

Shows how to decorate text with borders and shading.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
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
* class [ParagraphFormat](../)

