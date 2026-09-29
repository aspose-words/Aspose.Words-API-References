---
title: RunCollection indexer
linktitle: RunCollection indexer
articleTitle: RunCollection indexer
second_title: Aspose.Words for Python
description: "RunCollection indexer. Retrieves a [Run](../../run/) at the given index."
type: docs
weight: 10
url: /es/python-net/aspose.words/runcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [Run](../../run/) at the given index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




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

* module [aspose.words](../../)
* class [RunCollection](../)

