---
title: CompositeNode.get_child_nodes method
linktitle: get_child_nodes method
articleTitle: get_child_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.get_child_nodes method. Returns a live collection of child nodes that match the specified type."
type: docs
weight: 100
url: /es/python-net/aspose.words/compositenode/get_child_nodes/
---

## get_child_nodes(node_type, is_deep) {#nodetype_bool}

Returns a live collection of child nodes that match the specified type.


```python
def get_child_nodes(self, node_type: aspose.words.NodeType, is_deep: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node_type | [NodeType](../../nodetype/) | Specifies the type of nodes to select. |
| is_deep | bool | ``True`` to select from all child nodes recursively; ``False`` to select only among immediate children.  |

### Remarks

The collection of nodes returned by this method is always live.




A live collection is always in sync with the document. For example, if you
selected all sections in a document and enumerate through the collection
deleting the sections, the section is removed from the collection immediately
when it is removed from the document.




### Returns

A live collection of child nodes of the specified type.


### Examples

Shows how to print all of a document's comments and their replies.

```python
doc = aw.Document(file_name=MY_DIR + 'Comments.docx')
comments = doc.get_child_nodes(aw.NodeType.COMMENT, True)
# Si un comentario no tiene ancestro, es un comentario "de nivel superior" en contraste con un comentario de tipo respuesta.
# Imprima todos los comentarios de nivel superior junto con cualquier respuesta que puedan tener.
for comment in list(filter(lambda c: c.ancestor == None, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_comment(), b), list(comments)))))):
    print('Top-level comment:')
    print(f'\t"{comment.get_text().strip()}", by {comment.author}')
    print(f'Has {comment.replies.count} replies')
    for comment_reply in comment.replies:
        comment_reply = comment_reply.as_comment()
        print(f'\t"{comment_reply.get_text().strip()}", by {comment_reply.author}')
    print()
```

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()
# Agregar dos ejecuciones y una forma como nodos hijos al primer párrafo de este documento.
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc=doc, text='Hello world! '))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# Tenga en cuenta que el 'CustomNodeId' no se guarda en un archivo de salida y solo existe durante la vida del nodo.
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)
paragraph.append_child(aw.Run(doc=doc, text='Hello again!'))
# Itera a través de la colección de hijos inmediatos del párrafo,
# y muestra cualquier ejecución o forma que encontremos dentro.
children = paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, False).count)
for child in children:
    switch_condition = child.node_type
    if switch_condition == aw.NodeType.RUN:
        print('Run contents:')
        print(f'\t"{child.get_text().strip()}"')
    elif switch_condition == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print('Shape:')
        print(f'\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}')
```

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

