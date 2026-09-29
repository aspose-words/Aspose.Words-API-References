---
title: NodeCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "NodeCollection.clear method. Removes all nodes from this collection and from the document."
type: docs
weight: 40
url: /it/python-net/aspose.words/nodecollection/clear/
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
# Questo documento ha una sezione con alcuni nodi figlio che contengono e visualizzano tutti i contenuti del documento.
self.assertEqual(1, doc.sections.count)
self.assertEqual(17, doc.sections[0].get_child_nodes(aw.NodeType.ANY, True).count)
self.assertEqual('Hello World!\r\rHello Word!\r\r\rHello World!', doc.get_text().strip())
# Cancella la collezione di sezioni, il che rimuoverà tutti i figli del documento.
doc.sections.clear()
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.ANY, True).count)
self.assertEqual('', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

