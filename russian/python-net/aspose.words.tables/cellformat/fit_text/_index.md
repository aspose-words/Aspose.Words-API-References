---
title: CellFormat.fit_text property
linktitle: fit_text property
articleTitle: fit_text property
second_title: Aspose.Words for Python
description: "CellFormat.fit_text property. If ``True``, fits text in the cell, compressing each paragraph to the width of the cell."
type: docs
weight: 30
url: /ru/python-net/aspose.words.tables/cellformat/fit_text/
---

## CellFormat.fit_text property

If ``True``, fits text in the cell, compressing each paragraph to the width of the cell.



```python
@property
def fit_text(self) -> bool:
    ...

@fit_text.setter
def fit_text(self, value: bool):
    ...

```

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

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

