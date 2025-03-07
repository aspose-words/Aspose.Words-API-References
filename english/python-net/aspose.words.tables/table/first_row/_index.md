---
title: Table.first_row property
linktitle: first_row property
articleTitle: first_row property
second_title: Aspose.Words for Python
description: "Table.first_row property. Returns the first [Row](../../row/) node in the table."
type: docs
weight: 160
url: /python-net/aspose.words.tables/table/first_row/
---

## Table.first_row property

Returns the first [Row](../../row/) node in the table.



```python
@property
def first_row(self) -> aspose.words.tables.Row:
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

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# Below are two ways of getting a table from a document.
# 1 -  From the "Tables" collection of a Body node:
first_table = doc.first_section.body.tables[0]
# 2 -  Using the "GetChild" method:
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# Append all rows from the current table to the next.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# Remove the empty table container.
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

