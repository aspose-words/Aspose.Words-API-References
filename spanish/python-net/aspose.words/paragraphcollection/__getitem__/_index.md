---
title: ParagraphCollection indexer
linktitle: ParagraphCollection indexer
articleTitle: ParagraphCollection indexer
second_title: Aspose.Words for Python
description: "ParagraphCollection indexer. Retrieves a [Paragraph](../../paragraph/) at the given index."
type: docs
weight: 10
url: /es/python-net/aspose.words/paragraphcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [Paragraph](../../paragraph/) at the given index.



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

Shows how to check whether a paragraph is a move revision.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Este documento contiene revisiones "Move", que aparecen cuando resaltamos texto con el cursor,
# y luego lo arrastramos para moverlo a otra ubicación
# mientras se rastrean revisiones en Microsoft Word a través de "Review" -> "Track changes".
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Las revisiones de movimiento consisten en pares de revisiones "Move from" y "Move to".
# Estas revisiones son cambios potenciales en el documento que podemos aceptar o rechazar.
# Antes de aceptar/rechazar una revisión de movimiento, el documento
# debe llevar un registro de los destinos de salida y llegada del texto.
# El segundo y el cuarto párrafo definen una de esas revisiones, y por lo tanto ambos tienen el mismo contenido.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# La revisión "Move from" es el párrafo del que arrastramos el texto.
# Si aceptamos la revisión, este párrafo desaparecerá,
# y el otro permanecerá y ya no será una revisión.
self.assertTrue(paragraphs[1].is_move_from_revision)
# La revisión "Move to" es el párrafo al que arrastramos el texto.
# Si rechazamos la revisión, este párrafo en su lugar desaparecerá, y el otro permanecerá.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphCollection](../)

