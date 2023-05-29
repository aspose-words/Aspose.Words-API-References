---
title: Table.top_padding property
linktitle: top_padding property
articleTitle: top_padding property
second_title: Aspose.Words for Python
description: "Table.top_padding property. Gets or sets the amount of space (in points) to add above the contents of cells."
type: docs
weight: 330
url: /python-net/aspose.words.tables/table/top_padding/
---

## Table.top_padding property

Gets or sets the amount of space (in points) to add above the contents of cells.


### Examples

Shows how to configure content padding in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Row 1, cell 1.")
builder.insert_cell()
builder.write("Row 1, cell 2.")
builder.end_table()

# For every cell in the table, set the distance between its contents and each of its borders.
# This table will maintain the minimum padding distance by wrapping text.
table.left_padding = 30
table.right_padding = 60
table.top_padding = 10
table.bottom_padding = 90
table.preferred_width = aw.tables.PreferredWidth.from_points(250)

doc.save(ARTIFACTS_DIR + "Table.padding.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

