---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /es/python-net/aspose.words/documentbuilder/move_to/
---

## move_to(node) {#node}

Moves the cursor to an inline node or to the end of a paragraph.


```python
def move_to(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node must be a paragraph or a direct child of a paragraph. |

### Remarks

When *node* is an inline-level node, the cursor is moved to this node
and further content will be inserted before that node.

When *node* is a [Paragraph](../../paragraph/), the cursor is moved to the end of the paragraph
and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node
and further content will be inserted just before the paragraph break.




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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# El generador de documentos tiene un cursor, que actúa como la parte del documento
# donde el generador agrega nuevos nodos cuando usamos sus métodos de construcción de documentos.
# Este cursor funciona de la misma manera que el cursor intermitente de Microsoft Word,
# y también siempre termina inmediatamente después de cualquier nodo que el generador acaba de insertar.
# Para agregar contenido a una parte diferente del documento,
# podemos mover el cursor a un nodo diferente con el método "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# El cursor ahora está delante del nodo al que lo movimos.
# Agregar una segunda ejecución lo insertará delante de la primera ejecución.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Mueva el cursor al final del documento para continuar añadiendo texto al final como antes.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

