---
title: Cell.cell_format property
linktitle: cell_format property
articleTitle: cell_format property
second_title: Aspose.Words for Python
description: "Cell.cell_format property. Provides access to the formatting properties of the cell."
type: docs
weight: 20
url: /de/python-net/aspose.words.tables/cell/cell_format/
---

## Cell.cell_format property

Provides access to the formatting properties of the cell.


```python
@property
def cell_format(self) -> aspose.words.tables.CellFormat:
    ...

```

### Examples

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
# Verwenden Sie die "RowFormat"‑Eigenschaft der ersten Zeile, um die Formatierung zu ändern
# des Inhalts aller Zellen in dieser Zeile.
row_format = table.first_row.row_format
row_format.height = 25
row_format.borders.get_by_border_type(aw.BorderType.BOTTOM).color = aspose.pydrawing.Color.red
# Verwenden Sie die "CellFormat"‑Eigenschaft der ersten Zelle in der letzten Zeile, um die Formatierung des Inhalts dieser Zelle zu ändern.
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
# Verwenden Sie die "CellFormat"-Eigenschaft einer Zelle, um die Formatierung festzulegen, die das Aussehen dieser Zelle ändert.
first_cell.cell_format.width = 30
first_cell.cell_format.orientation = aw.TextOrientation.DOWNWARD
first_cell.cell_format.shading.foreground_pattern_color = aspose.pydrawing.Color.light_green
doc.save(file_name=ARTIFACTS_DIR + 'Table.CellFormat.docx')
```

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# Im Folgenden sind zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
# 1 -  Aus der "Tables"-Sammlung eines Body-Knotens:
first_table = doc.first_section.body.tables[0]
# 2 -  Verwendung der "GetChild"-Methode:
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# Fügen Sie alle Zeilen der aktuellen Tabelle an die nächste an.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# Entfernen Sie den leeren Tabellenkontainer.
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

