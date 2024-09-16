---
title: TextureIndex enumeration
linktitle: TextureIndex enumeration
articleTitle: TextureIndex enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TextureIndex enumeration. Specifies shading texture."
type: docs
weight: 1300
url: /python-net/aspose.words/textureindex/
---

## TextureIndex enumeration

Specifies shading texture.


### Members

| Name | Description |
| --- | --- |
| TEXTURE_10_PERCENT |  |
| TEXTURE_12PT5_PERCENT |  |
| TEXTURE_15_PERCENT |  |
| TEXTURE_17PT5_PERCENT |  |
| TEXTURE_20_PERCENT |  |
| TEXTURE_22PT5_PERCENT |  |
| TEXTURE_25_PERCENT |  |
| TEXTURE_27PT5_PERCENT |  |
| TEXTURE_2PT5_PERCENT |  |
| TEXTURE_30_PERCENT |  |
| TEXTURE_32PT5_PERCENT |  |
| TEXTURE_35_PERCENT |  |
| TEXTURE_37PT5_PERCENT |  |
| TEXTURE_40_PERCENT |  |
| TEXTURE_42PT5_PERCENT |  |
| TEXTURE_45_PERCENT |  |
| TEXTURE_47PT5_PERCENT |  |
| TEXTURE_50_PERCENT |  |
| TEXTURE_52PT5_PERCENT |  |
| TEXTURE_55_PERCENT |  |
| TEXTURE_57PT5_PERCENT |  |
| TEXTURE_5_PERCENT |  |
| TEXTURE_60_PERCENT |  |
| TEXTURE_62PT5_PERCENT |  |
| TEXTURE_65_PERCENT |  |
| TEXTURE_67PT5_PERCENT |  |
| TEXTURE_70_PERCENT |  |
| TEXTURE_72PT5_PERCENT |  |
| TEXTURE_75_PERCENT |  |
| TEXTURE_77PT5_PERCENT |  |
| TEXTURE_7PT5_PERCENT |  |
| TEXTURE_80_PERCENT |  |
| TEXTURE_82PT5_PERCENT |  |
| TEXTURE_85_PERCENT |  |
| TEXTURE_87PT5_PERCENT |  |
| TEXTURE_90_PERCENT |  |
| TEXTURE_92PT5_PERCENT |  |
| TEXTURE_95_PERCENT |  |
| TEXTURE_97PT5_PERCENT |  |
| TEXTURE_CROSS |  |
| TEXTURE_DARK_CROSS |  |
| TEXTURE_DARK_DIAGONAL_CROSS |  |
| TEXTURE_DARK_DIAGONAL_DOWN |  |
| TEXTURE_DARK_DIAGONAL_UP |  |
| TEXTURE_DARK_HORIZONTAL |  |
| TEXTURE_DARK_VERTICAL |  |
| TEXTURE_DIAGONAL_CROSS |  |
| TEXTURE_DIAGONAL_DOWN |  |
| TEXTURE_DIAGONAL_UP |  |
| TEXTURE_HORIZONTAL |  |
| TEXTURE_NONE |  |
| TEXTURE_SOLID |  |
| TEXTURE_VERTICAL |  |
| TEXTURE_NIL | Specifies that there shall be no pattern used on the current shaded region  (i.e. the pattern shall be a complete fill with the background color). |

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

Shows how to apply an outline border to a table.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# Align the table to the center of the page.
table.alignment = aw.tables.TableAlignment.CENTER
# Clear any existing borders and shading from the table.
table.clear_borders()
table.clear_shading()
# Add green borders to the outline of the table.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
# Fill the cells with a light green solid color.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, aspose.pydrawing.Color.light_green, aspose.pydrawing.Color.empty())
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetOutlineBorders.docx')
```

### See Also

* module [aspose.words](../)

