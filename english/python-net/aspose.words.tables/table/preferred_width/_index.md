﻿---
title: Table.preferred_width property
linktitle: preferred_width property
articleTitle: preferred_width property
second_title: Aspose.Words for Python
description: "Table.preferred_width property. Gets or sets the table preferred width."
type: docs
weight: 220
url: /python-net/aspose.words.tables/table/preferred_width/
---

## Table.preferred_width property

Gets or sets the table preferred width.


```python
@property
def preferred_width(self) -> aspose.words.tables.PreferredWidth:
    ...

@preferred_width.setter
def preferred_width(self, value: aspose.words.tables.PreferredWidth):
    ...

```

### Remarks

The default value is [PreferredWidth.AUTO](../../preferredwidth/AUTO/).




### Examples

Shows how to set a table to auto fit to 50% of the width of the page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Cell #1')
builder.insert_cell()
builder.write('Cell #2')
builder.insert_cell()
builder.write('Cell #3')
table.preferred_width = aw.tables.PreferredWidth.from_percent(50)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTableWithPreferredWidth.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

