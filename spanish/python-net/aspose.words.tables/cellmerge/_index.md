---
title: CellMerge enumeration
linktitle: CellMerge enumeration
articleTitle: CellMerge enumeration
second_title: Aspose.Words for Python
description: "aspose.words.tables.CellMerge enumeration. Specifies how a cell in a table is merged with other cells."
type: docs
weight: 50
url: /es/python-net/aspose.words.tables/cellmerge/
---

## CellMerge enumeration

Specifies how a cell in a table is merged with other cells.


### Members

| Name | Description |
| --- | --- |
| NONE | The cell is not merged. |
| FIRST | The cell is the first cell in a range of merged cells. |
| PREVIOUS | The cell is merged to the previous cell horizontally or vertically. |

### Examples

Shows how to merge table cells vertically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte una celda en la primera columna de la primera fila.
# Esta celda será la primera en un rango de celdas fusionadas verticalmente.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# Inserte una celda en la segunda columna de la primera fila, luego finalice la fila.
# Además, configure el generador para desactivar la fusión vertical en las celdas creadas.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
# Inserte una celda en la primera columna de la segunda fila.
# En lugar de añadir contenido de texto, fusionaremos esta celda con la primera celda que añadimos directamente arriba.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.PREVIOUS
# Inserte otra celda independiente en la segunda columna de la segunda fila.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'CellFormat.VerticalMerge.docx')
```

Shows how to merge table cells horizontally.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte una celda en la primera columna de la primera fila.
# Esta celda será la primera en un rango de celdas fusionadas horizontalmente.
builder.insert_cell()
builder.cell_format.horizontal_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# Inserte una celda en la segunda columna de la primera fila. En lugar de añadir contenido de texto,
# fusionaremos esta celda con la primera celda que añadimos directamente a la izquierda.
builder.insert_cell()
builder.cell_format.horizontal_merge = aw.tables.CellMerge.PREVIOUS
builder.end_row()
# Inserte dos celdas más sin fusionar en la segunda fila.
builder.cell_format.horizontal_merge = aw.tables.CellMerge.NONE
builder.insert_cell()
builder.write('Text in unmerged cell.')
builder.insert_cell()
builder.write('Text in unmerged cell.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'CellFormat.HorizontalMerge.docx')
```

Prints the horizontal and vertical merge type of a cell.

```python
doc = aw.Document(file_name=MY_DIR + 'Table with merged cells.docx')
table = doc.first_section.body.tables[0]
for row in table.rows:
    row = row.as_row()
    for cell in row.cells:
        cell = cell.as_cell()
        print(self.print_cell_merge_type(cell))
```

Prints the horizontal and vertical merge type of a cell (PrintCellMergeType).

```python
def print_cell_merge_type(self, cell):
    is_horizontally_merged = cell.cell_format.horizontal_merge != aw.tables.CellMerge.NONE
    is_vertically_merged = cell.cell_format.vertical_merge != aw.tables.CellMerge.NONE
    cell_location = f'R{cell.parent_row.parent_table.index_of(cell.parent_row) + 1}, C{cell.parent_row.index_of(cell) + 1}'
    if is_horizontally_merged and is_vertically_merged:
        return f'The cell at {cell_location} is both horizontally and vertically merged'
    if is_horizontally_merged:
        return f'The cell at {cell_location} is horizontally merged.'
    return f'The cell at {cell_location} is vertically merged' if is_vertically_merged else f'The cell at {cell_location} is not merged'
```

### See Also

* module [aspose.words.tables](../)

