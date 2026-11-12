---
title: DocumentBuilder.end_row method
linktitle: end_row method
articleTitle: end_row method
second_title: Aspose.Words for Python
description: "DocumentBuilder.end_row method. Ends a table row in the document."
type: docs
weight: 240
url: /ru/python-net/aspose.words/documentbuilder/end_row/
---

## end_row() {#default}

Ends a table row in the document.


```python
def end_row(self):
    ...
```

### Remarks

Call [DocumentBuilder.end_row()](./#default) to end a table row. If you call [DocumentBuilder.insert_cell()](../insert_cell/#default) immediately
after that, then the table continues on a new row.

Use the [DocumentBuilder.row_format](../row_format/) property to specify row formatting.




### Returns

The row node that was just finished.


### Examples

Shows how to merge table cells vertically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте ячейку в первый столбец первой строки.
# Эта ячейка будет первой в диапазоне вертикально объединённых ячеек.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# Вставьте ячейку во второй столбец первой строки, затем завершите строку.
# Также настройте построитель, чтобы отключить вертикальное объединение в созданных ячейках.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
# Вставьте ячейку в первый столбец второй строки.
# Вместо добавления текстового содержимого мы объединим эту ячейку с первой ячейкой, которую добавили непосредственно выше.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.PREVIOUS
# Вставьте другую независимую ячейку во второй столбец второй строки.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'CellFormat.VerticalMerge.docx')
```

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
# Во время построения таблицы документный построитель будет применять текущие значения свойств RowFormat/CellFormat
# к текущей строке/ячейке, в которой находится курсор, и к любым новым строкам/ячейкам, которые он создаёт.
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
# Ранее добавленные строки и ячейки не подвергаются ретроспективному изменению из‑за изменений форматирования построителя.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.BuildTable.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

