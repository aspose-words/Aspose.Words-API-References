---
title: CellVerticalAlignment enumeration
linktitle: CellVerticalAlignment enumeration
articleTitle: CellVerticalAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.tables.CellVerticalAlignment enumeration. Specifies vertical justification of text inside a table cell."
type: docs
weight: 60
url: /zh/python-net/aspose.words.tables/cellverticalalignment/
---

## CellVerticalAlignment enumeration

Specifies vertical justification of text inside a table cell.


### Members

| Name | Description |
| --- | --- |
| TOP | Text is aligned at the top of a cell. |
| CENTER | Text is aligned in the middle of a cell. |
| BOTTOM | Text is aligned at the bottom of the cell. |

### Examples

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

### See Also

* module [aspose.words.tables](../)

