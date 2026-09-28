---
title: Row.row_format property
linktitle: row_format property
articleTitle: row_format property
second_title: Aspose.Words for Python
description: "Row.row_format property. Provides access to the formatting properties of the row."
type: docs
weight: 120
url: /de/python-net/aspose.words.tables/row/row_format/
---

## Row.row_format property

Provides access to the formatting properties of the row.


```python
@property
def row_format(self) -> aspose.words.tables.RowFormat:
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

Shows how to modify formatting of a table row.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# Verwenden Sie die "RowFormat"‑Eigenschaft der ersten Zeile, um eine Formatierung festzulegen, die das gesamte Aussehen dieser Zeile ändert.
first_row = table.first_row
first_row.row_format.borders.line_style = aw.LineStyle.NONE
first_row.row_format.height_rule = aw.HeightRule.AUTO
first_row.row_format.allow_break_across_pages = True
doc.save(file_name=ARTIFACTS_DIR + 'Table.RowFormat.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Row](../)

