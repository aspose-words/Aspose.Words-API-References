---
title: TextColumnCollection.set_count method
linktitle: set_count method
articleTitle: set_count method
second_title: Aspose.Words for Python
description: "TextColumnCollection.set_count method. Arranges text into the specified number of text columns."
type: docs
weight: 70
url: /python-net/aspose.words/textcolumncollection/set_count/
---

## set_count(new_count) {#int}

Arranges text into the specified number of text columns.


```python
def set_count(self, new_count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_count | int |  |

When [TextColumnCollection.evenly_spaced](../evenly_spaced/) is ``False`` and you increase the number of columns,
new [TextColumn](../../textcolumn/) objects are created with zero width and spacing.
You need to set width and spacing for the new columns.




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

