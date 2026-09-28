---
title: RowFormat.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "RowFormat.clear_formatting method. Resets to default row formatting."
type: docs
weight: 60
url: /zh/python-net/aspose.words.tables/rowformat/clear_formatting/
---

## clear_formatting() {#default}

Resets to default row formatting.


```python
def clear_formatting(self):
    ...
```

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

### See Also

* module [aspose.words.tables](../../)
* class [RowFormat](../)

