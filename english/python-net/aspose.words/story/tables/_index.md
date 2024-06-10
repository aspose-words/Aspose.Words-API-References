---
title: Story.tables property
linktitle: tables property
articleTitle: tables property
second_title: Aspose.Words for Python
description: "Story.tables property. Gets a collection of tables that are immediate children of the story."
type: docs
weight: 50
url: /python-net/aspose.words/story/tables/
---

## Story.tables property

Gets a collection of tables that are immediate children of the story.


```python
@property
def tables(self) -> aspose.words.tables.TableCollection:
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

* module [aspose.words](../../)
* class [Story](../)

