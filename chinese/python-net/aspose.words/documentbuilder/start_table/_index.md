---
title: DocumentBuilder.start_table method
linktitle: start_table method
articleTitle: start_table method
second_title: Aspose.Words for Python
description: "DocumentBuilder.start_table method. Starts a table in the document."
type: docs
weight: 680
url: /zh/python-net/aspose.words/documentbuilder/start_table/
---

## start_table() {#default}

Starts a table in the document.


```python
def start_table(self):
    ...
```

### Remarks

The next method to call is [DocumentBuilder.insert_cell()](../insert_cell/#default).

This method starts a nested table when called inside a cell.




### Returns

The table node that was just created.


### Examples

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# 为文档构建器设置表格格式选项
# 将把它们应用于我们使用它添加的每一行和每个单元格。
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.cell_format.clear_formatting()
builder.cell_format.width = 150
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.green_yellow
builder.cell_format.wrap_text = False
builder.cell_format.fit_text = True
builder.row_format.clear_formatting()
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.row_format.height = 50
builder.row_format.borders.line_style = aw.LineStyle.ENGRAVE_3D
builder.row_format.borders.color = aspose.pydrawing.Color.orange
builder.insert_cell()
builder.write('Row 1, Col 1')
builder.insert_cell()
builder.write('Row 1, Col 2')
builder.end_row()
# 更改格式将把它应用于当前单元格，
# 以及我们随后使用构建器创建的任何新单元格。
# 这不会影响我们之前添加的单元格。
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# 增加行高以适应垂直文本。
builder.insert_cell()
builder.row_format.height = 150
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 3, Col 1')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 3, Col 2')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTable.docx')
```

Shows how to build a formatted 2x2 table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.write('Row 1, cell 1.')
builder.insert_cell()
builder.write('Row 1, cell 2.')
builder.end_row()
# 在构建表格时，文档构建器将应用其当前的 RowFormat/CellFormat 属性值
# 到光标所在的当前行/单元格以及在创建时的任何新行/单元格。
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[0].cell_format.vertical_alignment)
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[1].cell_format.vertical_alignment)
builder.insert_cell()
builder.row_format.height = 100
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 2, cell 1.')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 2, cell 2.')
builder.end_row()
builder.end_table()
# 先前添加的行和单元格不会因对构建器格式的更改而被追溯影响。
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.BuildTable.docx')
```

Shows how to format cells with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# 插入第二个单元格，然后配置单元格文本填充选项。
# 构建器将在当前单元格应用这些设置，随后创建的任何新单元格也会使用这些设置。
builder.insert_cell()
cell_format = builder.cell_format
cell_format.width = 250
cell_format.left_padding = 30
cell_format.right_padding = 30
cell_format.top_padding = 30
cell_format.bottom_padding = 30
builder.write('Row 1, cell 2.')
builder.end_row()
builder.end_table()
# 第一个单元格未受填充重新配置的影响，仍保持默认值。
self.assertEqual(0, table.first_row.cells[0].cell_format.width)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.left_padding)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.right_padding)
self.assertEqual(0, table.first_row.cells[0].cell_format.top_padding)
self.assertEqual(0, table.first_row.cells[0].cell_format.bottom_padding)
self.assertEqual(250, table.first_row.cells[1].cell_format.width)
self.assertEqual(30, table.first_row.cells[1].cell_format.left_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.right_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.top_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.bottom_padding)
# 第一个单元格仍会在输出文档中增长，以匹配其相邻单元格的大小。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetCellFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

