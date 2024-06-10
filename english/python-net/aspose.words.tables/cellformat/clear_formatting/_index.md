---
title: CellFormat.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "CellFormat.clear_formatting method. Resets to default cell formatting"
type: docs
weight: 160
url: /python-net/aspose.words.tables/cellformat/clear_formatting/
---

## clear_formatting() {#default}

Resets to default cell formatting. Does not change the width of the cell.


```python
def clear_formatting(self):
    ...
```

### Examples

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
* class [CellFormat](../)

