---
title: RowFormat class
linktitle: RowFormat class
articleTitle: RowFormat class
second_title: Aspose.Words for Python
description: "aspose.words.tables.RowFormat class. Represents all formatting for a table row"
type: docs
weight: 110
url: /zh/python-net/aspose.words.tables/rowformat/
---

## RowFormat class

Represents all formatting for a table row.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [allow_break_across_pages](./allow_break_across_pages/) | True if the text in a table row is allowed to split across a page break. |
| [borders](./borders/) | Gets the collection of default cell borders for the row. |
| [heading_format](./heading_format/) | True if the row is repeated as a table heading on every page when the table spans more than one page. |
| [height](./height/) | Gets or sets the height of the table row in points. |
| [height_rule](./height_rule/) | Gets or sets the rule for determining the height of the table row. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Resets to default row formatting. |

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

Shows how to modify the format of rows and cells in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('City')
builder.insert_cell()
builder.write('Country')
builder.end_row()
builder.insert_cell()
builder.write('London')
builder.insert_cell()
builder.write('U.K.')
builder.end_table()
# 使用第一行的 "RowFormat" 属性来修改格式
# 该行所有单元格内容的格式。
row_format = table.first_row.row_format
row_format.height = 25
row_format.borders.get_by_border_type(aw.BorderType.BOTTOM).color = aspose.pydrawing.Color.red
# 使用最后一行第一个单元格的 "CellFormat" 属性来修改该单元格内容的格式。
cell_format = table.last_row.first_cell.cell_format
cell_format.width = 100
cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
doc.save(file_name=ARTIFACTS_DIR + 'Table.RowCellFormat.docx')
```

Shows how to modify formatting of a table row.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# 使用第一行的 "RowFormat" 属性设置格式，以修改整行的外观。
first_row = table.first_row
first_row.row_format.borders.line_style = aw.LineStyle.NONE
first_row.row_format.height_rule = aw.HeightRule.AUTO
first_row.row_format.allow_break_across_pages = True
doc.save(file_name=ARTIFACTS_DIR + 'Table.RowFormat.docx')
```

### See Also

* module [aspose.words.tables](../)

