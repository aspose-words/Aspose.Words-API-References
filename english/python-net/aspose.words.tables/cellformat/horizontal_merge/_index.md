---
title: CellFormat.horizontal_merge property
linktitle: horizontal_merge property
articleTitle: horizontal_merge property
second_title: Aspose.Words for Python
description: "CellFormat.horizontal_merge property. Specifies how the cell is merged horizontally with other cells in the row."
type: docs
weight: 50
url: /python-net/aspose.words.tables/cellformat/horizontal_merge/
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
builder = aw.DocumentBuilder(doc)

# Insert a cell into the first column of the first row.
# This cell will be the first in a range of horizontally merged cells.
builder.insert_cell()
builder.cell_format.horizontal_merge = aw.tables.CellMerge.FIRST
builder.write("Text in merged cells.")

# Insert a cell into the second column of the first row. Instead of adding text contents,
# we will merge this cell with the first cell that we added directly to the left.
builder.insert_cell()
builder.cell_format.horizontal_merge = aw.tables.CellMerge.PREVIOUS
builder.end_row()

# Insert two more unmerged cells to the second row.
builder.cell_format.horizontal_merge = aw.tables.CellMerge.NONE
builder.insert_cell()
builder.write("Text in unmerged cell.")
builder.insert_cell()
builder.write("Text in unmerged cell.")
builder.end_row()
builder.end_table()

doc.save(ARTIFACTS_DIR + "CellFormat.horizontal_merge.docx")
```

Prints the horizontal and vertical merge type of a cell.

```python
def test_check_cells_merged(self):

    doc = aw.Document(MY_DIR + "Table with merged cells.docx")
    table = doc.first_section.body.tables[0]

    for row in table.rows:
        row = row.as_row()
        for cell in row.cells:
            cell = cell.as_cell()
            print(self.print_cell_merge_type(cell))

@staticmethod
def print_cell_merge_type(cell: aw.tables.Cell) -> str:

    is_horizontally_merged = cell.cell_format.horizontal_merge != aw.tables.CellMerge.NONE
    is_vertically_merged = cell.cell_format.vertical_merge != aw.tables.CellMerge.NONE
    cell_location = f"R{cell.parent_row.parent_table.index_of(cell.parent_row) + 1}, C{cell.parent_row.index_of(cell) + 1}"

    if is_horizontally_merged and is_vertically_merged:
        return f"The cell at {cell_location} is both horizontally and vertically merged"
    if is_horizontally_merged:
        return f"The cell at {cell_location} is horizontally merged."
    if is_vertically_merged:
        return f"The cell at {cell_location} is vertically merged"
    return f"The cell at {cell_location} is not merged"
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)
* property [CellFormat.vertical_merge](../vertical_merge/)

