---
title: Story.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for Python
description: "Story.paragraphs property. Gets a collection of paragraphs that are immediate children of the story."
type: docs
weight: 30
url: /de/python-net/aspose.words/story/paragraphs/
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
# Dieses Dokument enthält "Move"‑Revisionen, die erscheinen, wenn wir Text mit dem Cursor markieren,
# und ihn dann ziehen, um ihn an einen anderen Ort zu verschieben
# während Revisionen in Microsoft Word über "Review" → "Track changes" nachverfolgt werden.
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Move‑Revisionen bestehen aus Paaren von "Move from"‑ und "Move to"‑Revisionen.
# Diese Revisionen sind potenzielle Änderungen am Dokument, die wir entweder akzeptieren oder ablehnen können.
# Bevor wir eine Move‑Revision akzeptieren/ablehnen, muss das Dokument
# muss sowohl den Abgangs- als auch den Ankunftsort des Textes nachverfolgen.
# Der zweite und der vierte Absatz definieren eine solche Revision und haben daher denselben Inhalt.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# Die "Move from"‑Revision ist der Absatz, von dem wir den Text gezogen haben.
# Wenn wir die Revision akzeptieren, wird dieser Absatz verschwinden,
# und der andere bleibt erhalten und ist nicht mehr eine Revision.
self.assertTrue(paragraphs[1].is_move_from_revision)
# Die "Move to"‑Revision ist der Absatz, zu dem wir den Text gezogen haben.
# Wenn wir die Revision ablehnen, wird stattdessen dieser Absatz verschwinden, und der andere bleibt erhalten.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

