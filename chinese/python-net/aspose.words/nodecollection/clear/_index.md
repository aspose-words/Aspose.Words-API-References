---
title: NodeCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "NodeCollection.clear method. Removes all nodes from this collection and from the document."
type: docs
weight: 40
url: /zh/python-net/aspose.words/nodecollection/clear/
---

## clear() {#default}

Removes all nodes from this collection and from the document.


```python
def clear(self):
    ...
```

### Examples

Shows how to remove all sections from a document.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
# 此文档有一个节，其中包含一些子节点，承载并显示文档的全部内容。
self.assertEqual(1, doc.sections.count)
self.assertEqual(17, doc.sections[0].get_child_nodes(aw.NodeType.ANY, True).count)
self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', doc.get_text().strip())
# 清除节集合，这将删除文档的所有子项。
doc.sections.clear()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.ANY, True).count)
self.assertEqual('', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

