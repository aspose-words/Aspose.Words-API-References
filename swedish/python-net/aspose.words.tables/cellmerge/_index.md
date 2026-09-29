---
title: CellMerge enumeration
linktitle: CellMerge enumeration
articleTitle: CellMerge enumeration
second_title: Aspose.Words for Python
description: "aspose.words.tables.CellMerge enumeration. Specifies how a cell in a table is merged with other cells."
type: docs
weight: 50
url: /sv/python-net/aspose.words.tables/cellmerge/
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
# Infoga en cell i den första kolumnen i den första raden.
# Denna cell kommer att vara den första i ett område av vertikalt sammanslagna celler.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# Infoga en cell i den andra kolumnen i den första raden, avsluta sedan raden.
# Konfigurera också byggaren för att inaktivera vertikal sammanslagning i skapade celler.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
# Infoga en cell i den första kolumnen i den andra raden.
# Istället för att lägga till textinnehåll kommer vi att slå samman den här cellen med den första cellen som vi lade till direkt ovanför.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.PREVIOUS
# Infoga en annan oberoende cell i den andra kolumnen i den andra raden.
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
# Infoga en cell i den första kolumnen i den första raden.
# Denna cell kommer att vara den första i ett område av horisontellt sammanslagna celler.
builder.insert_cell()
builder.cell_format.horizontal_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# Infoga en cell i den andra kolumnen i den första raden. Istället för att lägga till textinnehåll,
# kommer vi att slå samman den här cellen med den första cellen som vi lade till direkt till vänster.
builder.insert_cell()
builder.cell_format.horizontal_merge = aw.tables.CellMerge.PREVIOUS
builder.end_row()
# Infoga två ytterligare osammanslagna celler till den andra raden.
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

