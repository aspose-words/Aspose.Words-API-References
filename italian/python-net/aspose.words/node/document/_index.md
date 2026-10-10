---
title: Node.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "Node.document property. Gets the document to which this node belongs."
type: docs
weight: 20
url: /it/python-net/aspose.words/node/document/
---

## Node.document property

Gets the document to which this node belongs.


```python
@property
def document(self) -> aspose.words.DocumentBase:
    ...

```

### Remarks

The node always belongs to a document even if it has just been created
and not yet added to the tree, or if it has been removed from the tree.




### Examples

Shows how to create a node and set its owning document.

```python
from api_example_base import ApiExampleBase
doc = aw.Document()
para = aw.Paragraph(doc)
para.append_child(aw.Run(doc=doc, text='Hello world!'))
# Non abbiamo ancora aggiunto questo paragrafo come figlio a nessun nodo composito.
self.assertIsNone(para.parent_node)
# Se un nodo è un tipo di nodo figlio appropriato di un altro nodo composito,
# possiamo collegarlo come figlio solo se entrambi i nodi hanno lo stesso documento proprietario.
# Il documento proprietario è il documento che abbiamo passato al costruttore del nodo.
# Non abbiamo allegato questo paragrafo al documento, quindi il documento non contiene il suo testo.
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# Poiché il documento possiede questo paragrafo, possiamo applicare uno dei suoi stili al contenuto del paragrafo.
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# Aggiungi questo nodo al documento, quindi verifica il suo contenuto.
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

