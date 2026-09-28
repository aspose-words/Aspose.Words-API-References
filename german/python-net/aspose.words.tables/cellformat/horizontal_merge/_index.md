---
title: CellFormat.horizontal_merge property
linktitle: horizontal_merge property
articleTitle: horizontal_merge property
second_title: Aspose.Words for Python
description: "CellFormat.horizontal_merge property. Specifies how the cell is merged horizontally with other cells in the row."
type: docs
weight: 50
url: /de/python-net/aspose.words.tables/cellformat/horizontal_merge/
---

## CellFormat.horizontal_merge property

Specifies how the cell is merged horizontally with other cells in the row.


```python
@property
def horizontal_merge(self) -> aspose.words.tables.CellMerge:
    ...

@horizontal_merge.setter
def horizontal_merge(self, value: aspose.words.tables.CellMerge):
    ...

```

### Examples

Shows how to merge table cells horizontally.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie eine Zelle in die erste Spalte der ersten Zeile ein.
# Diese Zelle wird die erste in einem Bereich von horizontal zusammengeführten Zellen sein.
builder.insert_cell()
builder.cell_format.horizontal_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# Fügen Sie eine Zelle in die zweite Spalte der ersten Zeile ein. Anstatt Textinhalte hinzuzufügen,
# werden wir diese Zelle mit der ersten Zelle zusammenführen, die wir direkt links hinzugefügt haben.
builder.insert_cell()
builder.cell_format.horizontal_merge = aw.tables.CellMerge.PREVIOUS
builder.end_row()
# Fügen Sie der zweiten Zeile zwei weitere nicht zusammengeführte Zellen hinzu.
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

* module [aspose.words.tables](../../)
* class [CellFormat](../)
* property [CellFormat.vertical_merge](../vertical_merge/)

