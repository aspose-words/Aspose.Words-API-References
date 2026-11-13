---
title: CellFormat.wrap_text property
linktitle: wrap_text property
articleTitle: wrap_text property
second_title: Aspose.Words for Python
description: "CellFormat.wrap_text property. If ``True``, wrap text for the cell."
type: docs
weight: 150
url: /es/python-net/aspose.words.tables/cellformat/wrap_text/
---

## CellFormat.wrap_text property

If ``True``, wrap text for the cell.



```python
@property
def wrap_text(self) -> bool:
    ...

@wrap_text.setter
def wrap_text(self, value: bool):
    ...

```

### Examples

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# Configurando opciones de formato de tabla para un constructor de documentos
# se aplicarán a cada fila y celda que agreguemos con él.
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
# Cambiar el formato lo aplicará a la celda actual,
# y cualquier celda nueva que creemos con el builder después.
# Esto no afectará a las celdas que hemos añadido previamente.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# Aumente la altura de la fila para que se ajuste al texto vertical.
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

