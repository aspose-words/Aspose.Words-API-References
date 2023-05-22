---
title: Cell.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Cell.last_paragraph property. Gets the last paragraph among the immediate children."
type: docs
weight: 60
url: /python-net/aspose.words.tables/cell/last_paragraph/
---

## Cell.last_paragraph property

Gets the last paragraph among the immediate children.


### Examples

Shows how to apply settings to vertical borders to a table row's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a table with red and blue inner borders.
table = builder.start_table()

for i in range(3):
    builder.insert_cell()
    builder.write(f"Row {i + 1}, Column 1")
    builder.insert_cell()
    builder.write(f"Row {i + 1}, Column 2")

    row = builder.end_row()
    borders = row.row_format.borders

    # Adjust the appearance of borders that will appear between rows.
    borders.horizontal.color = drawing.Color.red
    borders.horizontal.line_style = aw.LineStyle.DOT
    borders.horizontal.line_width = 2.0

    # Adjust the appearance of borders that will appear between cells.
    borders.vertical.color = drawing.Color.blue
    borders.vertical.line_style = aw.LineStyle.DOT
    borders.vertical.line_width = 2.0

# A row format, and a cell's inner paragraph use different border settings.
border = table.first_row.first_cell.last_paragraph.paragraph_format.borders.vertical

self.assertEqual(drawing.Color.empty().to_argb(), border.color.to_argb())
self.assertEqual(0.0, border.line_width)
self.assertEqual(aw.LineStyle.NONE, border.line_style)

doc.save(ARTIFACTS_DIR + "Border.vertical_borders.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

