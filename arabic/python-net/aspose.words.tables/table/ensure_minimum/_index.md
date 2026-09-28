---
title: Table.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Table.ensure_minimum method. If the table has no rows, creates and appends one [Row](../../row/)."
type: docs
weight: 420
url: /ar/python-net/aspose.words.tables/table/ensure_minimum/
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
# الجداول تحتوي على صفوف، والتي تحتوي على خلايا، والتي قد تحتوي على فقرات
# مع عناصر نمطية مثل النصوص المتتابعة، الأشكال، وحتى جداول أخرى.
# جدولنا الجديد لا يحتوي على أي من هذه العقد، ولا يمكننا إضافة محتوى إليه حتى يتم إنشاؤها.
self.assertEqual(0, table.get_child_nodes(aw.NodeType.ANY, True).count)
# استدعاء طريقة "EnsureMinimum" على جدول سيضمن أن
# الجدول يحتوي على صف واحد على الأقل وخلية واحدة مع فقرة فارغة.
table.ensure_minimum()
table.first_row.first_cell.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

