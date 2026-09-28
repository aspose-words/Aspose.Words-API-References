---
title: Table.set_border method
linktitle: set_border method
articleTitle: set_border method
second_title: Aspose.Words for Python
description: "Table.set_border method. Sets the specified table border to the specified line style, width and color."
type: docs
weight: 430
url: /zh/python-net/aspose.words.tables/table/set_border/
---

## set_border(border_type, line_style, line_width, color, is_override_cell_borders) {#bordertype_linestyle_float_color_bool}

Sets the specified table border to the specified line style, width and color.


```python
def set_border(self, border_type: aspose.words.BorderType, line_style: aspose.words.LineStyle, line_width: float, color: aspose.pydrawing.Color, is_override_cell_borders: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| border_type | [BorderType](../../../aspose.words/bordertype/) | The table border to change. |
| line_style | [LineStyle](../../../aspose.words/linestyle/) | The line style to apply. |
| line_width | float | The line width to set (in points). |
| color | aspose.pydrawing.Color | The color to use for the border. |
| is_override_cell_borders | bool | When ``True``, causes all existing explicit cell borders to be removed. |

### Examples

Shows how to apply an outline border to a table.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# 将表格对齐到页面中心。
table.alignment = aw.tables.TableAlignment.CENTER
# 清除表格中任何现有的边框和阴影。
table.clear_borders()
table.clear_shading()
# 为表格的轮廓添加绿色边框。
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
# 用淡绿色实色填充单元格。
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, aspose.pydrawing.Color.light_green, aspose.pydrawing.Color.empty())
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetOutlineBorders.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

