---
title: InlineStory.is_delete_revision property
linktitle: is_delete_revision property
articleTitle: is_delete_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_delete_revision property. Returns true if this object was deleted in Microsoft Word while change tracking was enabled."
type: docs
weight: 30
url: /es/python-net/aspose.words/inlinestory/is_delete_revision/
---

## InlineStory.is_delete_revision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.


```python
@property
def is_delete_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision footnotes.docx')
# Cuando editamos el documento mientras la opción "Track Changes", encontrada en Revisar -> Seguimiento,
# está activada en Microsoft Word, los cambios que aplicamos cuentan como revisiones.
# Al editar un documento usando Aspose.Words, podemos comenzar a rastrear revisiones mediante
# invocando el método "StartTrackRevisions" del documento y deteniendo el seguimiento mediante el método "StopTrackRevisions".
# Podemos aceptar las revisiones para asimilarlas al documento
# o rechácelos para deshacer y descartar el cambio propuesto.
self.assertTrue(doc.has_revisions)
footnotes = list(map(lambda x: x.as_footnote(), list(doc.get_child_nodes(aw.NodeType.FOOTNOTE, True))))
self.assertEqual(5, len(footnotes))
# A continuación se presentan cinco tipos de revisiones que pueden marcar un nodo InlineStory.
# 1 -  Una revisión "insert":
# Esta revisión ocurre cuando insertamos texto mientras se rastrean los cambios.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  Una revisión de "move from":
# Cuando resaltamos texto en Microsoft Word y luego lo arrastramos a un lugar diferente en el documento
# mientras se rastrean los cambios, aparecen dos revisiones.
# La revisión "move from" es una copia del texto original antes de moverlo.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  Una revisión de "move to":
# La revisión "move to" es el texto que movimos a su nueva posición en el documento.
# Las revisiones "move from" y "move to" aparecen en pares para cada revisión de movimiento que realizamos.
# Aceptar una revisión de movimiento elimina la revisión "move from" y su texto,
# y conserva el texto de la revisión "move to".
# Rechazar una revisión de movimiento, por el contrario, conserva la revisión "move from" y elimina la revisión "move to".
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  Una revisión de "delete":
# Esta revisión ocurre cuando eliminamos texto mientras se rastrean los cambios. Cuando eliminamos texto de esta manera,
# permanecerá en el documento como una revisión hasta que aceptemos la revisión,
# lo que eliminará el texto de forma permanente, o rechazará la revisión, lo que mantendrá el texto que eliminamos donde estaba.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

