---
title: text_columns property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns a collection that represents the set of text columns."
type: docs
weight: 410
url: /python-net/aspose.words/pagesetup/text_columns/
---

## PageSetup.text_columns property

Returns a collection that represents the set of text columns.


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
* class [PageSetup](../)

