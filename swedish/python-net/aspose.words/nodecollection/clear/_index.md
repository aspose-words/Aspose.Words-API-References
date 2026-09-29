---
title: NodeCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "NodeCollection.clear method. Removes all nodes from this collection and from the document."
type: docs
weight: 40
url: /sv/python-net/aspose.words/nodecollection/clear/
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
# Detta dokument har en sektion med några barnnoder som innehåller och visar hela dokumentets innehåll.
self.assertEqual(1, doc.sections.count)
self.assertEqual(17, doc.sections[0].get_child_nodes(aw.NodeType.ANY, True).count)
self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', doc.get_text().strip())
# Rensa samlingen av sektioner, vilket kommer att ta bort alla dokumentets barn.
doc.sections.clear()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.ANY, True).count)
self.assertEqual('', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

