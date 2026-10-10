---
title: CellFormat.left_padding property
linktitle: left_padding property
articleTitle: left_padding property
second_title: Aspose.Words for Python
description: "CellFormat.left_padding property. Returns or sets the amount of space (in points) to add to the left of the contents of cell."
type: docs
weight: 60
url: /zh/python-net/aspose.words.tables/cellformat/left_padding/
---

## CellFormat.left_padding property

Returns or sets the amount of space (in points) to add to the left of the contents of cell.


```python
@property
def left_padding(self) -> float:
    ...

@left_padding.setter
def left_padding(self, value: float):
    ...

```

### Examples

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

* module [aspose.words.tables](../../)
* class [CellFormat](../)

