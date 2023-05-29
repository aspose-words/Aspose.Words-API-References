---
title: TextColumn.space_after property
linktitle: space_after property
articleTitle: space_after property
second_title: Aspose.Words for Python
description: "TextColumn.space_after property. Gets or sets the space between this column and the next column in points"
type: docs
weight: 10
url: /python-net/aspose.words/textcolumn/space_after/
---

## TextColumn.space_after property

Gets or sets the space between this column and the next column in points. Not required for the last column.


### Examples

Shows how to create unevenly spaced columns.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
page_setup = builder.page_setup

columns = page_setup.text_columns
columns.evenly_spaced = False
columns.set_count(2)

# Determine the amount of room that we have available for arranging columns.
content_width = page_setup.page_width - page_setup.left_margin - page_setup.right_margin

self.assertAlmostEqual(470.30, content_width, delta=0.01)

# Set the first column to be narrow.
column = columns[0]
column.width = 100
column.space_after = 20

# Set the second column to take the rest of the space available within the margins of the page.
column = columns[1]
column.width = content_width - column.width - column.space_after

builder.writeln("Narrow column 1.")
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln("Wide column 2.")

doc.save(ARTIFACTS_DIR + "PageSetup.custom_column_width.docx")
```

### See Also

* module [aspose.words](../../)
* class [TextColumn](../)

