---
title: CellFormat.vertical_merge property
linktitle: vertical_merge property
articleTitle: vertical_merge property
second_title: Aspose.Words for Python
description: "CellFormat.vertical_merge property. Specifies how the cell is merged with other cells vertically."
type: docs
weight: 130
url: /zh/python-net/aspose.words.tables/cellformat/vertical_merge/
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
builder = aw.DocumentBuilder(doc=doc)
# 在第一行的第一列插入一个单元格。
# 此单元格将是垂直合并单元格范围中的第一个。
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# 在第一行的第二列插入一个单元格，然后结束该行。
# 此外，配置构建器以在创建的单元格中禁用垂直合并。
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
# 在第二行的第一列插入一个单元格。
# 我们将不添加文本内容，而是将此单元格与直接在上方添加的第一个单元格合并。
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.PREVIOUS
# 在第二行的第二列插入另一个独立的单元格。
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'CellFormat.VerticalMerge.docx')
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
* property [CellFormat.horizontal_merge](../horizontal_merge/)

