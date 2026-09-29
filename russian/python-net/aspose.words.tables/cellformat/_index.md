---
title: CellFormat class
linktitle: CellFormat class
articleTitle: CellFormat class
second_title: Aspose.Words for Python
description: "aspose.words.tables.CellFormat class. Represents all formatting for a table cell"
type: docs
weight: 40
url: /ru/python-net/aspose.words.tables/cellformat/
---

## CellFormat class

Represents all formatting for a table cell.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [borders](./borders/) | Gets collection of borders of the cell. |
| [bottom_padding](./bottom_padding/) | Returns or sets the amount of space (in points) to add below the contents of cell. |
| [fit_text](./fit_text/) | If ``True``, fits text in the cell, compressing each paragraph to the width of the cell. |
| [hide_mark](./hide_mark/) | Returns or sets visibility of cell mark. |
| [horizontal_merge](./horizontal_merge/) | Specifies how the cell is merged horizontally with other cells in the row. |
| [left_padding](./left_padding/) | Returns or sets the amount of space (in points) to add to the left of the contents of cell. |
| [orientation](./orientation/) | Returns or sets the orientation of text in a table cell. |
| [preferred_width](./preferred_width/) | Returns or sets the preferred width of the cell. |
| [right_padding](./right_padding/) | Returns or sets the amount of space (in points) to add to the right of the contents of cell. |
| [shading](./shading/) | Returns a [Shading](../../aspose.words/shading/) object that refers to the shading formatting for the cell. |
| [top_padding](./top_padding/) | Returns or sets the amount of space (in points) to add above the contents of cell. |
| [vertical_alignment](./vertical_alignment/) | Returns or sets the vertical alignment of text in the cell. |
| [vertical_merge](./vertical_merge/) | Specifies how the cell is merged with other cells vertically. |
| [width](./width/) | Gets the width of the cell in points. |
| [wrap_text](./wrap_text/) | If ``True``, wrap text for the cell. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Resets to default cell formatting. Does not change the width of the cell. |
|[ set_paddings(left_padding, top_padding, right_padding, bottom_padding)](./set_paddings/#float_float_float_float) | Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell. |

### Examples

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# Установка параметров форматирования таблицы для построителя документа
# будет применять их к каждой строке и ячейке, которые мы добавляем с его помощью.
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
# Изменение форматирования применит его к текущей ячейке,
# и любые новые ячейки, которые мы создаём с помощью построителя позже.
# Это не повлияет на ячейки, которые мы добавили ранее.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# Увеличьте высоту строки, чтобы разместить вертикальный текст.
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
# Используйте свойство "RowFormat" первой строки, чтобы изменить форматирование
# содержимого всех ячеек в этой строке.
row_format = table.first_row.row_format
row_format.height = 25
row_format.borders.get_by_border_type(aw.BorderType.BOTTOM).color = aspose.pydrawing.Color.red
# Используйте свойство "CellFormat" первой ячейки последней строки, чтобы изменить форматирование содержимого этой ячейки.
cell_format = table.last_row.first_cell.cell_format
cell_format.width = 100
cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
doc.save(file_name=ARTIFACTS_DIR + 'Table.RowCellFormat.docx')
```

Shows how to modify formatting of a table cell.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
first_cell = table.first_row.first_cell
# Используйте свойство "CellFormat" ячейки, чтобы задать форматирование, изменяющее внешний вид этой ячейки.
first_cell.cell_format.width = 30
first_cell.cell_format.orientation = aw.TextOrientation.DOWNWARD
first_cell.cell_format.shading.foreground_pattern_color = aspose.pydrawing.Color.light_green
doc.save(file_name=ARTIFACTS_DIR + 'Table.CellFormat.docx')
```

### See Also

* module [aspose.words.tables](../)

