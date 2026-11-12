---
title: IStructuredDocumentTag.remove_self_only method
linktitle: remove_self_only method
articleTitle: remove_self_only method
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.remove_self_only method. Removes just this SDT node itself, but keeps the content of it inside the document tree."
type: docs
weight: 180
url: /ru/python-net/aspose.words.markup/istructureddocumenttag/remove_self_only/
---

## remove_self_only() {#default}

Removes just this SDT node itself, but keeps the content of it inside the document tree.


```python
def remove_self_only(self):
    ...
```

### Examples

Shows how to remove structured document tag, but keeps content inside.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags.docx')
# Эта коллекция предоставляет единый интерфейс для доступа к диапазонным и недиапазонным структурированным тегам.
sdts = list(doc.range.structured_document_tags)
self.assertEqual(5, len(sdts))
# Здесь мы можем получить дочерние узлы через общий интерфейс диапазонных и недиапазонных структурированных тегов.
for sdt in sdts:
    if sdt.get_child_nodes(aw.NodeType.ANY, False).count > 0:
        sdt.remove_self_only()
sdts = list(doc.range.structured_document_tags)
self.assertEqual(0, len(sdts))
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

