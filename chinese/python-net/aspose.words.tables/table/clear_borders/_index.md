---
title: Table.clear_borders method
linktitle: clear_borders method
articleTitle: clear_borders method
second_title: Aspose.Words for Python
description: "Table.clear_borders method. Removes all table and cell borders on this table."
type: docs
weight: 390
url: /zh/python-net/aspose.words.tables/table/clear_borders/
---

## clear_borders() {#default}

Removes all table and cell borders on this table.


```python
def clear_borders(self):
    ...
```

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

Shows how to remove all borders from a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Hello world!')
builder.end_table()
# 修改顶部边框的颜色和粗细。
top_border = table.first_row.row_format.borders.get_by_border_type(aw.BorderType.TOP)
table.set_border(aw.BorderType.TOP, aw.LineStyle.DOUBLE, 1.5, aspose.pydrawing.Color.red, True)
self.assertEqual(1.5, top_border.line_width)
self.assertEqual(aspose.pydrawing.Color.red.to_argb(), top_border.color.to_argb())
self.assertEqual(aw.LineStyle.DOUBLE, top_border.line_style)
# 清除表格中所有单元格的边框，然后保存文档。
table.clear_borders()
doc.save(file_name=ARTIFACTS_DIR + 'Table.ClearBorders.docx')
# 重新打开文档后，验证表格属性的值。
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Table.ClearBorders.docx')
table = doc.first_section.body.tables[0]
top_border = table.first_row.row_format.borders.get_by_border_type(aw.BorderType.TOP)
self.assertEqual(0, top_border.line_width)
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), top_border.color.to_argb())
self.assertEqual(aw.LineStyle.NONE, top_border.line_style)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

