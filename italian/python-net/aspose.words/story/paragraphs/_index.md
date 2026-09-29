---
title: Story.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for Python
description: "Story.paragraphs property. Gets a collection of paragraphs that are immediate children of the story."
type: docs
weight: 30
url: /it/python-net/aspose.words/story/paragraphs/
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
# Questo documento contiene revisioni "Move", che appaiono quando evidenziamo il testo con il cursore,
# e poi lo trasciniamo per spostarlo in un'altra posizione
# mentre tracciamo le revisioni in Microsoft Word tramite "Review" -> "Track changes".
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Le revisioni Move consistono in coppie di revisioni "Move from" e "Move to".
# Queste revisioni sono modifiche potenziali al documento che possiamo accettare o rifiutare.
# Prima di accettare/rifiutare una revisione di spostamento, il documento
# deve tenere traccia sia della destinazione di partenza che di quella di arrivo del testo.
# Il secondo e il quarto paragrafo definiscono una tale revisione, e quindi entrambi hanno lo stesso contenuto.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# La revisione "Move from" è il paragrafo da cui abbiamo trascinato il testo.
# Se accettiamo la revisione, questo paragrafo scomparirà,
# e l'altro rimarrà e non sarà più una revisione.
self.assertTrue(paragraphs[1].is_move_from_revision)
# La revisione "Move to" è il paragrafo verso cui abbiamo trascinato il testo.
# Se rifiutiamo la revisione, questo paragrafo invece scomparirà, e l'altro rimarrà.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

