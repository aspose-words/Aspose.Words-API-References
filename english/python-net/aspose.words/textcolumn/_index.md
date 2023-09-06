﻿---
title: TextColumn class
linktitle: TextColumn class
articleTitle: TextColumn class
second_title: Aspose.Words for Python
description: "aspose.words.TextColumn class. Represents a single text column"
type: docs
weight: 1220
url: /python-net/aspose.words/textcolumn/
---

## TextColumn class

Represents a single text column. [TextColumn](./) is a member of the [TextColumnCollection](../textcolumncollection/) collection.
The [TextColumn](./) collection includes all the columns in a section of a document.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/python-net/working-with-sections/) documentation article.




[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want
the columns in the document to be of equal width, set TextColumns.[TextColumnCollection.evenly_spaced](../textcolumncollection/evenly_spaced/) to ``True``.

When a new [TextColumn](./) is created it has its width and spacing set to zero.




### Properties

| Name | Description |
| --- | --- |
| [space_after](./space_after/) | Gets or sets the space between this column and the next column in points. Not required for the last column. |
| [width](./width/) | Gets or sets the width of the text column in points. |

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

* module [aspose.words](../)
* class [TextColumnCollection](../textcolumncollection/)
* class [PageSetup](../pagesetup/)
* class [Section](../section/)

