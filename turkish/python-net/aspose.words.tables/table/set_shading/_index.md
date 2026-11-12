---
title: Table.set_shading method
linktitle: set_shading method
articleTitle: set_shading method
second_title: Aspose.Words for Python
description: "Table.set_shading method. Sets shading to the specified values on whole table."
type: docs
weight: 450
url: /tr/python-net/aspose.words.tables/table/set_shading/
---

## set_shading(texture, foreground_color, background_color) {#textureindex_color_color}

Sets shading to the specified values on whole table.


```python
def set_shading(self, texture: aspose.words.TextureIndex, foreground_color: aspose.pydrawing.Color, background_color: aspose.pydrawing.Color):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| texture | [TextureIndex](../../../aspose.words/textureindex/) | The texture to apply. |
| foreground_color | aspose.pydrawing.Color | The color of the texture. |
| background_color | aspose.pydrawing.Color | The color of the background fill. |

### Examples

Shows how to apply an outline border to a table.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# Tabloyu sayfanın ortasına hizalayın.
table.alignment = aw.tables.TableAlignment.CENTER
# Tablodaki mevcut kenarlıkları ve gölgelendirmeyi temizleyin.
table.clear_borders()
table.clear_shading()
# Tablonun dış hatlarına yeşil kenarlıklar ekleyin.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
# Hücreleri açık yeşil katı bir renk ile doldurun.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, aspose.pydrawing.Color.light_green, aspose.pydrawing.Color.empty())
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetOutlineBorders.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

