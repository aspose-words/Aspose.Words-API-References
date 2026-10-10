---
title: Cell.cell_format property
linktitle: cell_format property
articleTitle: cell_format property
second_title: Aspose.Words for Python
description: "Cell.cell_format property. Provides access to the formatting properties of the cell."
type: docs
weight: 20
url: /it/python-net/aspose.words.tables/cell/cell_format/
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
# Usa la proprietà "RowFormat" della prima riga per modificare la formattazione
# del contenuto di tutte le celle in questa riga.
row_format = table.first_row.row_format
row_format.height = 25
row_format.borders.get_by_border_type(aw.BorderType.BOTTOM).color = aspose.pydrawing.Color.red
# Usa la proprietà "CellFormat" della prima cella nell'ultima riga per modificare la formattazione del contenuto di quella cella.
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
# Usa la proprietà "CellFormat" di una cella per impostare la formattazione che modifica l'aspetto di quella cella.
first_cell.cell_format.width = 30
first_cell.cell_format.orientation = aw.TextOrientation.DOWNWARD
first_cell.cell_format.shading.foreground_pattern_color = aspose.pydrawing.Color.light_green
doc.save(file_name=ARTIFACTS_DIR + 'Table.CellFormat.docx')
```

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# Di seguito sono due modi per ottenere una tabella da un documento.
# 1 -  Dalla collezione "Tables" di un nodo Body:
first_table = doc.first_section.body.tables[0]
# 2 -  Usando il metodo "GetChild":
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# Aggiungi tutte le righe dalla tabella corrente a quella successiva.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# Rimuovi il contenitore della tabella vuota.
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

