---
title: preferred_width property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the table preferred width."
type: docs
weight: 220
url: /python-net/aspose.words.tables/table/preferred_width/
---

## Table.preferred_width property

Gets or sets the table preferred width.

The default value is [PreferredWidth.AUTO](../../preferredwidth/AUTO/).




### Examples

Shows how to set a table to auto fit to 50% of the width of the page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Cell #1")
builder.insert_cell()
builder.write("Cell #2")
builder.insert_cell()
builder.write("Cell #3")

table.preferred_width = aw.tables.PreferredWidth.from_percent(50)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_table_with_preferred_width.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

