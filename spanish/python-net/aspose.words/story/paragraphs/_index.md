---
title: Story.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for Python
description: "Story.paragraphs property. Gets a collection of paragraphs that are immediate children of the story."
type: docs
weight: 30
url: /es/python-net/aspose.words/story/paragraphs/
---

## Story.paragraphs property

Gets a collection of paragraphs that are immediate children of the story.


```python
@property
def paragraphs(self) -> aspose.words.ParagraphCollection:
    ...

```

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
* class [Story](../)

