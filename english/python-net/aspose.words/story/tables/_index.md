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
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
tables = doc.first_section.body.tables
self.assertEqual(5, tables[0].rows.count)
self.assertEqual(4, tables[1].rows.count)
for table in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_table(), b), list(tables))):
    cond_expression = table.first_row
    if cond_expression != None:
        cond_expression.remove()
    cond_expression2 = table.last_row
    if cond_expression2 != None:
        cond_expression2.remove()
self.assertEqual(3, tables[0].rows.count)
self.assertEqual(2, tables[1].rows.count)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

