---
title: NodeCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "NodeCollection.add method. Adds a node to the end of the collection."
type: docs
weight: 30
url: /es/python-net/aspose.words/nodecollection/add/
---

## add(node) {#node}

Adds a node to the end of the collection.


```python
def add(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node to be added to the end of the collection. |

### Remarks

The node is inserted as a child into the node object from which the collection was created.




If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(NotSupportedException)) | The [NodeCollection](../) is a "deep" collection. |

### Examples

Shows how to prepare a new section node for editing.

```python
doc = aw.Document()
# Un documento en blanco viene con una sección, que tiene un cuerpo, que a su vez tiene un párrafo.
# Podemos añadir contenido a este documento añadiendo elementos como ejecuciones de texto, formas o tablas a ese párrafo.
self.assertEqual(aw.NodeType.SECTION, doc.get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.BODY, doc.sections[0].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[0].body.get_child(aw.NodeType.ANY, 0, True).node_type)
# Si añadimos una nueva sección así, no tendrá un cuerpo, ni ningún otro nodo hijo.
doc.sections.add(aw.Section(doc))
self.assertEqual(0, doc.sections[1].get_child_nodes(aw.NodeType.ANY, True).count)
# Ejecute el método "EnsureMinimum" para añadir un cuerpo y un párrafo a esta sección y comenzar a editarla.
doc.last_section.ensure_minimum()
self.assertEqual(aw.NodeType.BODY, doc.sections[1].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[1].body.get_child(aw.NodeType.ANY, 0, True).node_type)
doc.sections[0].body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

