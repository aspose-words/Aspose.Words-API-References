---
title: Node.parent_node property
linktitle: parent_node property
articleTitle: parent_node property
second_title: Aspose.Words for Python
description: "Node.parent_node property. Gets the immediate parent of this node."
type: docs
weight: 60
url: /es/python-net/aspose.words/node/parent_node/
---

## Node.parent_node property

Gets the immediate parent of this node.


```python
@property
def parent_node(self) -> aspose.words.CompositeNode:
    ...

```

### Remarks

If a node has just been created and not yet added to the tree,
or if it has been removed from the tree, the parent is ``None``.




### Examples

Shows how to create a node and set its owning document.

```python
from api_example_base import ApiExampleBase
doc = aw.Document()
para = aw.Paragraph(doc)
para.append_child(aw.Run(doc=doc, text='Hello world!'))
# Aún no hemos añadido este párrafo como hijo a ningún nodo compuesto.
self.assertIsNone(para.parent_node)
# Si un nodo es un tipo de nodo hijo apropiado de otro nodo compuesto,
# podemos adjuntarlo como hijo solo si ambos nodos tienen el mismo documento propietario.
# El documento propietario es el documento que pasamos al constructor del nodo.
# No hemos adjuntado este párrafo al documento, por lo que el documento no contiene su texto.
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# Dado que el documento posee este párrafo, podemos aplicar uno de sus estilos al contenido del párrafo.
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# Agregue este nodo al documento y luego verifique su contenido.
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

