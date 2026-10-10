---
title: CompositeNode.prepend_child method
linktitle: prepend_child method
articleTitle: prepend_child method
second_title: Aspose.Words for Python
description: "CompositeNode.prepend_child method. Adds the specified node to the beginning of the list of child nodes for this node."
type: docs
weight: 150
url: /es/python-net/aspose.words/compositenode/prepend_child/
---

## prepend_child(new_child) {#node}

Adds the specified node to the beginning of the list of child nodes for this node.


```python
def prepend_child(self, new_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The node to add. |

### Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The node added.


### Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()
# Un documento vacío, por defecto, tiene un párrafo.
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# Los nodos compuestos, como nuestro párrafo, pueden contener otros nodos compuestos e inline como hijos.
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc=doc, text='Initial text. ')
paragraph.append_child(paragraph_text)
# Crea tres nodos de ejecución adicionales.
run1 = aw.Run(doc=doc, text='Run 1. ')
run2 = aw.Run(doc=doc, text='Run 2. ')
run3 = aw.Run(doc=doc, text='Run 3. ')
# El cuerpo del documento no mostrará estas ejecuciones hasta que las insertemos en un nodo compuesto
# que a su vez es parte del árbol de nodos del documento, como hicimos con la primera ejecución.
# Podemos determinar dónde aparecen los contenidos de texto de los nodos que insertamos
# en el documento al especificar una ubicación de inserción relativa a otro nodo en el párrafo.
self.assertEqual('Initial text.', paragraph.get_text().strip())
# Inserta la segunda ejecución en el párrafo delante de la ejecución inicial.
paragraph.insert_before(run2, paragraph_text)
self.assertEqual('Run 2. Initial text.', paragraph.get_text().strip())
# Inserta la tercera ejecución después de la ejecución inicial.
paragraph.insert_after(run3, paragraph_text)
self.assertEqual('Run 2. Initial text. Run 3.', paragraph.get_text().strip())
# Inserta la primera ejecución al inicio de la colección de nodos hijos del párrafo.
paragraph.prepend_child(run1)
self.assertEqual('Run 1. Run 2. Initial text. Run 3.', paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
# Podemos modificar el contenido de la ejecución editando y eliminando los nodos hijos existentes.
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = 'Updated run 2. '
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)
self.assertEqual('Run 1. Updated run 2. Run 3.', paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

