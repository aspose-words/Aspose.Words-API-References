---
title: Table.text_wrapping property
linktitle: text_wrapping property
articleTitle: text_wrapping property
second_title: Aspose.Words for Python
description: "Table.text_wrapping property. Gets or sets [Table.text_wrapping](./) for table."
type: docs
weight: 310
url: /python-net/aspose.words.tables/table/text_wrapping/
---

## Table.text_wrapping property

Gets or sets [Table.text_wrapping](./) for table.



### Examples

Shows how to work with table text wrapping.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Cell 1")
builder.insert_cell()
builder.write("Cell 2")
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)

builder.font.size = 16
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

# Set the "text_wrapping" property to "TextWrapping.AROUND" to get the table to wrap text around it,
# and push it down into the paragraph below by setting the position.
table.text_wrapping = aw.tables.TextWrapping.AROUND
table.absolute_horizontal_distance = 100
table.absolute_vertical_distance = 20

doc.save(ARTIFACTS_DIR + "Table.wrap_text.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

