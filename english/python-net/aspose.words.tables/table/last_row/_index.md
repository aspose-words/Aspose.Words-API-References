---
title: Table.last_row property
linktitle: last_row property
articleTitle: last_row property
second_title: Aspose.Words for Python
description: "Table.last_row property. Returns the last [Row](../../row/) node in the table."
type: docs
weight: 180
url: /python-net/aspose.words.tables/table/last_row/
---

## Table.last_row property

Returns the last [Row](../../row/) node in the table.



```python
@property
def last_row(self) -> aspose.words.tables.Row:
    ...

```

### Examples

Shows how to remove the first and last rows of all tables in a document.

```python
doc = aw.Document(MY_DIR + 'Tables.docx')
tables = doc.first_section.body.tables
self.assertEqual(5, tables[0].rows.count)
self.assertEqual(4, tables[1].rows.count)
for table in tables:
    table = table.as_table()
    if table.first_row is not None:
        table.first_row.remove()
    if table.last_row is not None:
        table.last_row.remove()
self.assertEqual(3, tables[0].rows.count)
self.assertEqual(2, tables[1].rows.count)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

