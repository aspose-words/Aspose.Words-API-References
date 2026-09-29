---
title: CellFormat.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for Python
description: "CellFormat.borders property. Gets collection of borders of the cell."
type: docs
weight: 10
url: /ru/python-net/aspose.words.tables/cellformat/borders/
---

## CellFormat.borders property

Gets collection of borders of the cell.


```python
@property
def borders(self) -> aspose.words.BorderCollection:
    ...

```

### Examples

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# Ниже представлены два способа получения таблицы из документа.
# 1 -  Из коллекции \"Tables\" узла Body:
first_table = doc.first_section.body.tables[0]
# 2 -  С использованием метода \"GetChild\":
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# Добавьте все строки из текущей таблицы к следующей.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# Удалите пустой контейнер таблицы.
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

