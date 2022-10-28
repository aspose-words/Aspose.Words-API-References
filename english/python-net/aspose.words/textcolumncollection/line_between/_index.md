---
title: line_between property
second_title: Aspose.Words for Python via .NET API Reference
description: "When ``True``, adds a vertical line between columns."
type: docs
weight: 40
url: /python-net/aspose.words/textcolumncollection/line_between/
---

## TextColumnCollection.line_between property

When ``True``, adds a vertical line between columns.



### Examples

Shows how to separate columns with a vertical line.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Configure the current section's PageSetup object to divide the text into several columns.
# Set the "line_between" property to "True" to put a dividing line between columns.
# Set the "line_between" property to "False" to leave the space between columns blank.
columns = builder.page_setup.text_columns
columns.line_between = line_between
columns.set_count(3)

builder.writeln("Column 1.")
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln("Column 2.")
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln("Column 3.")

doc.save(ARTIFACTS_DIR + "PageSetup.vertical_line_between_columns.docx")
```

### See Also

* module [aspose.words](../../)
* class [TextColumnCollection](../)

