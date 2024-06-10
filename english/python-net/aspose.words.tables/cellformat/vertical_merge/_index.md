---
title: CellFormat.vertical_merge property
linktitle: vertical_merge property
articleTitle: vertical_merge property
second_title: Aspose.Words for Python
description: "CellFormat.vertical_merge property. Specifies how the cell is merged with other cells vertically."
type: docs
weight: 130
url: /python-net/aspose.words.tables/cellformat/vertical_merge/
---

## CellFormat.vertical_merge property

Specifies how the cell is merged with other cells vertically.


```python
@property
def vertical_merge(self) -> aspose.words.tables.CellMerge:
    ...

@vertical_merge.setter
def vertical_merge(self, value: aspose.words.tables.CellMerge):
    ...

```

### Remarks

Cells can only be merged vertically if their left and right boundaries are identical.

When cells are vertically merged, the display areas of the merged cells are consolidated.
The consolidated area is used to display the contents of the first vertically merged cell
and all other vertically merged cells must be empty.




### Examples

Shows how to merge table cells vertically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a cell into the first column of the first row.
# This cell will be the first in a range of vertically merged cells.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# Insert a cell into the second column of the first row, then end the row.
# Also, configure the builder to disable vertical merging in created cells.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
# Insert a cell into the first column of the second row.
# Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.PREVIOUS
# Insert another independent cell in the second column of the second row.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'CellFormat.VerticalMerge.docx')
```

Prints the horizontal and vertical merge type of a cell.

```python
def check_cells_merged():
    doc = aw.Document(MY_DIR + 'Table with merged cells.docx')
    table = doc.first_section.body.tables[0]
    for row in table.rows:
        row = row.as_row()
        for cell in row.cells:
            cell = cell.as_cell()
            print(print_cell_merge_type(cell))

def print_cell_merge_type(cell: aw.tables.Cell) -> str:
    is_horizontally_merged = cell.cell_format.horizontal_merge != aw.tables.CellMerge.NONE
    is_vertically_merged = cell.cell_format.vertical_merge != aw.tables.CellMerge.NONE
    cell_location = f'R{cell.parent_row.parent_table.index_of(cell.parent_row) + 1}, C{cell.parent_row.index_of(cell) + 1}'
    if is_horizontally_merged and is_vertically_merged:
        return f'The cell at {cell_location} is both horizontally and vertically merged'
    if is_horizontally_merged:
        return f'The cell at {cell_location} is horizontally merged.'
    if is_vertically_merged:
        return f'The cell at {cell_location} is vertically merged'
    return f'The cell at {cell_location} is not merged'
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)
* property [CellFormat.horizontal_merge](../horizontal_merge/)

