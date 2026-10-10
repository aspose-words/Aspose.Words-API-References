---
title: CellFormat.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "CellFormat.clear_formatting method. Resets to default cell formatting"
type: docs
weight: 160
url: /de/python-net/aspose.words.tables/cellformat/clear_formatting/
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
# Im Folgenden sind zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
# 1 -  Aus der "Tables"-Sammlung eines Body-Knotens:
first_table = doc.first_section.body.tables[0]
# 2 -  Verwendung der "GetChild"-Methode:
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# Fügen Sie alle Zeilen der aktuellen Tabelle an die nächste an.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# Entfernen Sie den leeren Tabellenkontainer.
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

