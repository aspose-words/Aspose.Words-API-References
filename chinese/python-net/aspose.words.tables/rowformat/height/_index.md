---
title: RowFormat.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "RowFormat.height property. Gets or sets the height of the table row in points."
type: docs
weight: 40
url: /zh/python-net/aspose.words.tables/rowformat/height/
---

## RowFormat.height property

Gets or sets the height of the table row in points.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
    ...

```

### Examples

Shows how to create a formatted table using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
table.left_indent = 20
# 设置一些文本和表格外观的格式选项。
builder.row_format.height = 40
builder.row_format.height_rule = aw.HeightRule.AT_LEAST
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.from_argb(198, 217, 241)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.font.size = 16
builder.font.name = 'Arial'
builder.font.bold = True
# 在文档生成器中配置格式选项将会应用它们
# 到光标所在的当前单元格/行，
# 以及使用该生成器创建的任何新单元格和行。
builder.write('Header Row,\n Cell 1')
builder.insert_cell()
builder.write('Header Row,\n Cell 2')
builder.insert_cell()
builder.write('Header Row,\n Cell 3')
builder.end_row()
# 重新配置生成器的格式对象，以用于我们即将创建的新行和单元格。
# 生成器不会将这些应用于已经创建的第一行，以使其突出显示为标题行。
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.white
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.row_format.height = 30
builder.row_format.height_rule = aw.HeightRule.AUTO
builder.insert_cell()
builder.font.size = 12
builder.font.bold = False
builder.write('Row 1, Cell 1.')
builder.insert_cell()
builder.write('Row 1, Cell 2.')
builder.insert_cell()
builder.write('Row 1, Cell 3.')
builder.end_row()
builder.insert_cell()
builder.write('Row 2, Cell 1.')
builder.insert_cell()
builder.write('Row 2, Cell 2.')
builder.insert_cell()
builder.write('Row 2, Cell 3.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateFormattedTable.docx')
```

Shows how to format rows with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# 启动第二行，然后配置其高度。构建器将把这些设置应用于
# 它当前的行以及之后创建的任何新行。
builder.end_row()
row_format = builder.row_format
row_format.height = 100
row_format.height_rule = aw.HeightRule.EXACTLY
builder.insert_cell()
builder.write('Row 2, cell 1.')
builder.end_table()
# 第一行未受填充重新配置的影响，仍保持默认值。
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetRowFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [RowFormat](../)

