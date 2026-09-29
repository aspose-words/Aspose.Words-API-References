---
title: CellFormat.preferred_width property
linktitle: preferred_width property
articleTitle: preferred_width property
second_title: Aspose.Words for Python
description: "CellFormat.preferred_width property. Returns or sets the preferred width of the cell."
type: docs
weight: 80
url: /es/python-net/aspose.words.tables/cellformat/preferred_width/
---

## CellFormat.preferred_width property

Returns or sets the preferred width of the cell.


```python
@property
def preferred_width(self) -> aspose.words.tables.PreferredWidth:
    ...

@preferred_width.setter
def preferred_width(self, value: aspose.words.tables.PreferredWidth):
    ...

```

### Remarks

The preferred width (along with the table's Auto Fit option) determines how the actual
width of the cell is calculated by the table layout algorithm. Table layout can be performed by
Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width
can also be specified as "auto", which means no preferred width is specified.

The default value is [PreferredWidth.AUTO](../../preferredwidth/AUTO/).




### Examples

Shows how to set a preferred width for table cells.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
# Hay dos formas de aplicar la clase "PreferredWidth" a las celdas de la tabla.
# 1 -  Establezca un ancho preferido absoluto basado en puntos:
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_points(40)
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_yellow
builder.writeln(f'Cell with a width of {builder.cell_format.preferred_width}.')
# 2 -  Establezca un ancho preferido relativo basado en el porcentaje del ancho de la tabla:
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_percent(20)
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_blue
builder.writeln(f'Cell with a width of {builder.cell_format.preferred_width}.')
builder.insert_cell()
# Una celda sin ancho preferido especificado ocupará el resto del espacio disponible.
builder.cell_format.preferred_width = aw.tables.PreferredWidth.AUTO
# Cada configuración de la propiedad "PreferredWidth" crea un nuevo objeto.
self.assertNotEqual(hash(table.first_row.cells[1].cell_format.preferred_width), hash(builder.cell_format.preferred_width))
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_green
builder.writeln('Automatically sized cell.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertCellsWithPreferredWidths.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)
* property [CellFormat.width](../width/)

