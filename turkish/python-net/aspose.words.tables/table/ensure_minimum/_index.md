---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 420
url: /tr/python-net/aspose.words.tables/table/ensure_minimum/
---

## ensure_minimum() {#default}

If the table has no rows, creates and appends one [Row](../../row/).



```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to ensure that a table node contains the nodes we need to add content.

```python
doc = aw.Document()
table = aw.tables.Table(doc)
doc.first_section.body.append_child(table)
# Tablolar satırları içerir, satırlar hücreleri içerir, hücreler ise paragrafları içerebilir
# koşumlar, şekiller ve hatta diğer tablolar gibi tipik öğelerle
# Yeni tablomuz bu düğümlerden hiçbirine sahip değil ve bu düğümler oluşana kadar ona içerik ekleyemeyiz.
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)
# Bir tablo üzerinde "EnsureMinimum" yöntemini çağırmak, şunun sağlanmasını garantiler
# tablonun en az bir satırı ve boş bir paragraf içeren bir hücresi vardır.
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

