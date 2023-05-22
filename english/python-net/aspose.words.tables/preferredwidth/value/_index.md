---
title: PreferredWidth.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "PreferredWidth.value property. Gets the preferred width value"
type: docs
weight: 30
url: /python-net/aspose.words.tables/preferredwidth/value/
---

## PreferredWidth.value property

Gets the preferred width value. The unit of measure is specified in the [PreferredWidth.type](../type/) property.



### Examples

Shows how to verify the preferred width type and value of a table cell.

```python
doc = aw.Document(MY_DIR + "Tables.docx")

table = doc.first_section.body.tables[0]
first_cell = table.first_row.first_cell

self.assertEqual(aw.tables.PreferredWidthType.PERCENT, first_cell.cell_format.preferred_width.type)
self.assertEqual(11.16, first_cell.cell_format.preferred_width.value)
```

### See Also

* module [aspose.words.tables](../../)
* class [PreferredWidth](../)

