---
title: Table.absolute_horizontal_distance property
linktitle: absolute_horizontal_distance property
articleTitle: absolute_horizontal_distance property
second_title: Aspose.Words for Python
description: "Table.absolute_horizontal_distance property. Gets or sets absolute horizontal floating table position specified by the table properties, in points"
type: docs
weight: 20
url: /es/python-net/aspose.words.tables/table/absolute_horizontal_distance/
---

## Table.absolute_horizontal_distance property

Gets or sets absolute horizontal floating table position specified by the table properties, in points.
Default value is 0.


```python
@property
def absolute_horizontal_distance(self) -> float:
    ...

@absolute_horizontal_distance.setter
def absolute_horizontal_distance(self, value: float):
    ...

```

### Examples

Shows how set the location of floating tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Table 1, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# Establezca la ubicación de la tabla en un lugar de la página, como, en este caso, la esquina inferior derecha.
table.relative_vertical_alignment = aw.drawing.VerticalAlignment.BOTTOM
table.relative_horizontal_alignment = aw.drawing.HorizontalAlignment.RIGHT
table = builder.start_table()
builder.insert_cell()
builder.write('Table 2, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# También podemos establecer un desplazamiento horizontal y vertical en puntos desde la ubicación del párrafo donde insertamos la tabla.
table.absolute_vertical_distance = 50
table.absolute_horizontal_distance = 100
doc.save(file_name=ARTIFACTS_DIR + 'Table.ChangeFloatingTableProperties.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

