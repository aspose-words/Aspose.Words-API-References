---
title: DocumentBuilder.move_to_document_start method
linktitle: move_to_document_start method
articleTitle: move_to_document_start method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_document_start method. Moves the cursor to the beginning of the document."
type: docs
weight: 560
url: /es/python-net/aspose.words/documentbuilder/move_to_document_start/
---

## move_to_document_start() {#default}

Moves the cursor to the beginning of the document.


```python
def move_to_document_start(self):
    ...
```

### Examples

Shows how to move a document builder's cursor to different nodes in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crear un marcador válido, una entidad que consiste en nodos encerrados por un nodo de inicio de marcador,
# y un nodo de fin de marcador.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# El cursor del constructor de documentos siempre está delante del nodo que añadimos por última vez con él.
# Si el cursor del constructor está al final del documento, su nodo actual será nulo.
# El nodo anterior es el nodo de fin de marcador que añadimos por última vez.
# Agregar nuevos nodos con el constructor los añadirá al último nodo.
self.assertIsNone(builder.current_node)
# Si deseamos editar una parte diferente del documento con el constructor,
# necesitaremos llevar su cursor al nodo que deseamos editar.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# Moverlo a un marcador lo trasladará al primer nodo dentro de los nodos de inicio y fin de marcador, la ejecución encerrada.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# También podemos mover el cursor a un nodo individual de esta manera.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# Podemos usar métodos específicos para movernos al inicio/final de un documento.
builder.move_to_document_end()
self.assertTrue(builder.is_at_end_of_paragraph)
builder.move_to_document_start()
self.assertTrue(builder.is_at_start_of_paragraph)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

