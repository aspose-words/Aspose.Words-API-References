---
title: BorderCollection.horizontal property
linktitle: horizontal property
articleTitle: horizontal property
second_title: Aspose.Words for Python
description: "BorderCollection.horizontal property. Gets the horizontal border that is used between cells or conforming paragraphs."
type: docs
weight: 60
url: /python-net/aspose.words/bordercollection/horizontal/
---

## BorderCollection.horizontal property

Gets the horizontal border that is used between cells or conforming paragraphs.


### Examples

Shows how to apply settings to horizontal borders to a paragraph's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a red horizontal border for the paragraph. Any paragraphs created afterwards will inherit these border settings.
borders = doc.first_section.body.first_paragraph.paragraph_format.borders
borders.horizontal.color = drawing.Color.red
borders.horizontal.line_style = aw.LineStyle.DASH_SMALL_GAP
borders.horizontal.line_width = 3

# Write text to the document without creating a new paragraph afterward.
# Since there is no paragraph underneath, the horizontal border will not be visible.
builder.write("Paragraph above horizontal border.")

# Once we add a second paragraph, the border of the first paragraph will become visible.
builder.insert_paragraph()
builder.write("Paragraph below horizontal border.")

doc.save(ARTIFACTS_DIR + "Border.horizontal_borders.docx")
```

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

* module [aspose.words](../../)
* class [BorderCollection](../)

