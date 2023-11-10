---
title: PreferredWidth.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "PreferredWidth.type property. Gets the unit of measure used for this preferred width value."
type: docs
weight: 20
url: /python-net/aspose.words.tables/preferredwidth/type/
---

## PreferredWidth.type property

Gets the unit of measure used for this preferred width value.


```python
@property
def type(self) -> aspose.words.tables.PreferredWidthType:
    ...

```

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

