---
title: CellFormat.borders property
linktitle: borders property
articleTitle: borders property
second_title: Aspose.Words for Python
description: "CellFormat.borders property. Gets collection of borders of the cell."
type: docs
weight: 10
url: /tr/python-net/aspose.words.tables/cellformat/borders/
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
# Aşağıda bir belgeden tablo almanın iki yolu verilmiştir.
# 1 -  Bir Body düğümünün "Tables" koleksiyonundan:
first_table = doc.first_section.body.tables[0]
# 2 -  "GetChild" yöntemini kullanarak:
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# Mevcut tablodan tüm satırları sonraki tabloya ekleyin.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# Boş tablo kapsayıcısını kaldırın.
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

