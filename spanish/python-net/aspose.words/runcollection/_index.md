---
title: RunCollection class
linktitle: RunCollection class
articleTitle: RunCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RunCollection class. Provides typed access to a collection of [Run](../run/) nodes"
type: docs
weight: 1120
url: /es/python-net/aspose.words/runcollection/
---

## RunCollection class

Provides typed access to a collection of [Run](../run/) nodes.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




**Inheritance:** [RunCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Run](../run/) at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ index_of(node)](../nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove_at(index)](../nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ to_array()](./to_array/#default) | Copies all runs from the collection to a new array of runs. |

### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# Cuando editamos el documento mientras la opción "Track Changes", encontrada en Revisar -> Seguimiento,
# está activada en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
# Al editar un documento usando Aspose.Words, podemos comenzar a rastrear revisiones mediante
# invocando el método "StartTrackRevisions" del documento y deteniendo el seguimiento mediante el método "StopTrackRevisions".
# Podemos aceptar las revisiones para asimilarlas al documento
# o rechazarlas para modificar el cambio propuesto de manera efectiva.
self.assertEqual(6, doc.revisions.count)
# El nodo padre de una revisión es la ejecución (run) a la que la revisión se refiere. Un Run es un nodo Inline.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# A continuación se presentan cinco tipos de revisiones que pueden marcar un nodo Inline.
# 1 -  Una revisión "insert":
# Esta revisión ocurre cuando insertamos texto mientras se rastrean los cambios.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Una revisión "format":
# Esta revisión ocurre cuando cambiamos el formato del texto mientras se rastrean los cambios.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Una revisión "move from":
# Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a un lugar diferente en el documento
# mientras se rastrean los cambios, aparecen dos revisiones.
# La revisión "move from" es una copia del texto original antes de moverlo.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Una revisión "move to":
# La revisión "move to" es el texto que movimos a su nueva posición en el documento.
# Las revisiones "move from" y "move to" aparecen en pares para cada revisión de movimiento que realizamos.
# Aceptar una revisión de movimiento elimina la revisión "move from" y su texto,
# y conserva el texto de la revisión "move to".
# Rechazar una revisión de movimiento, por el contrario, conserva la revisión "move from" y elimina la revisión "move to".
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Una revisión "delete":
# Esta revisión ocurre cuando eliminamos texto mientras se rastrean los cambios. Cuando eliminamos texto de esta manera,
# permanecerá en el documento como una revisión hasta que aceptemos la revisión,
# lo que eliminará el texto de forma permanente, o rechazará la revisión, lo que mantendrá el texto que eliminamos donde estaba.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

