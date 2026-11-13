---
title: PreferredWidth.from_percent method
linktitle: from_percent method
articleTitle: from_percent method
second_title: Aspose.Words for Python
description: "PreferredWidth.from_percent method. A creation method that returns a new instance that represents a preferred width specified as a percentage."
type: docs
weight: 50
url: /es/python-net/aspose.words.tables/preferredwidth/from_percent/
---

## from_percent(percent) {#float}

A creation method that returns a new instance that represents a preferred width specified as a percentage.


```python
def from_percent(self, percent: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| percent | float | The value must be from 0 to 100. |

### Examples

Shows how to set a table to auto fit to 50% of the width of the page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Cell #1')
builder.insert_cell()
builder.write('Cell #2')
builder.insert_cell()
builder.write('Cell #3')
table.preferred_width = aw.tables.PreferredWidth.from_percent(50)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTableWithPreferredWidth.docx')
```

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
* class [PreferredWidth](../)

