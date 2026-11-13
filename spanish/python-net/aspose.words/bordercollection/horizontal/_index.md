---
title: BorderCollection.horizontal property
linktitle: horizontal property
articleTitle: horizontal property
second_title: Aspose.Words for Python
description: "BorderCollection.horizontal property. Gets the horizontal border that is used between cells or conforming paragraphs."
type: docs
weight: 60
url: /es/python-net/aspose.words/bordercollection/horizontal/
---

## BorderCollection.horizontal property

Gets the horizontal border that is used between cells or conforming paragraphs.


```python
@property
def horizontal(self) -> aspose.words.Border:
    ...

```

### Examples

Shows how to apply settings to horizontal borders to a paragraph's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un borde horizontal rojo para el párrafo. Cualquier párrafo creado después heredará esta configuración de borde.
borders = doc.first_section.body.first_paragraph.paragraph_format.borders
borders.horizontal.color = aspose.pydrawing.Color.red
borders.horizontal.line_style = aw.LineStyle.DASH_SMALL_GAP
borders.horizontal.line_width = 3
# Escribe texto en el documento sin crear un nuevo párrafo después.
# Dado que no hay un párrafo debajo, el borde horizontal no será visible.
builder.write('Paragraph above horizontal border.')
# Una vez que añadamos un segundo párrafo, el borde del primer párrafo se volverá visible.
builder.insert_paragraph()
builder.write('Paragraph below horizontal border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.HorizontalBorders.docx')
```

Shows how to apply settings to vertical borders to a table row's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea una tabla con bordes internos rojos y azules.
table = builder.start_table()
i = 0
while i < 3:
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 1')
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 2')
    row = builder.end_row()
    borders = row.row_format.borders
    # Ajusta la apariencia de los bordes que aparecerán entre filas.
    borders.horizontal.color = aspose.pydrawing.Color.red
    borders.horizontal.line_style = aw.LineStyle.DOT
    borders.horizontal.line_width = 2
    # Ajusta la apariencia de los bordes que aparecerán entre celdas.
    borders.vertical.color = aspose.pydrawing.Color.blue
    borders.vertical.line_style = aw.LineStyle.DOT
    borders.vertical.line_width = 2
    i += 1
# Un formato de fila y el párrafo interno de una celda usan configuraciones de borde diferentes.
border = table.first_row.first_cell.last_paragraph.paragraph_format.borders.vertical
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), border.color.to_argb())
self.assertEqual(0, border.line_width)
self.assertEqual(aw.LineStyle.NONE, border.line_style)
doc.save(file_name=ARTIFACTS_DIR + 'Border.VerticalBorders.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

