---
title: spacing property
second_title: Aspose.Words for Python via .NET API Reference
description: "When columns are evenly spaced, gets or sets the amount of space between each column in points."
type: docs
weight: 50
url: /python-net/aspose.words/textcolumncollection/spacing/
---

## TextColumnCollection.spacing property

When columns are evenly spaced, gets or sets the amount of space between each column in points.

Has effect only when [TextColumnCollection.evenly_spaced](../evenly_spaced/) is set to ``True``.



### Examples

Shows how to create multiple evenly spaced columns in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

columns = builder.page_setup.text_columns
columns.spacing = 100
columns.set_count(2)

builder.writeln("Column 1.")
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln("Column 2.")

doc.save(ARTIFACTS_DIR + "PageSetup.columns_same_width.docx")
```

### See Also

* module [aspose.words](../../)
* class [TextColumnCollection](../)

