---
title: Story.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for Python
description: "Story.paragraphs property. Gets a collection of paragraphs that are immediate children of the story."
type: docs
weight: 30
url: /sv/python-net/aspose.words/story/paragraphs/
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
# Detta dokument innehåller "Move"-revisioner, som visas när vi markerar text med markören,
# och sedan drar vi den för att flytta den till en annan plats
# medan vi spårar revisioner i Microsoft Word via "Review" -> "Track changes".
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Move-revisioner består av par av "Move from"- och "Move to"-revisioner.
# Dessa revisioner är potentiella förändringar i dokumentet som vi kan antingen acceptera eller avvisa.
# Innan vi accepterar/avvisar en move-revision, dokumentet
# måste hålla reda på både avrese- och ankomstdestinationerna för texten.
# Det andra och det fjärde stycket definierar en sådan revision, och därför har båda samma innehåll.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# "Move from"-revisionen är det stycke där vi drog texten från.
# Om vi accepterar revisionen kommer detta stycke att försvinna,
# och det andra kommer att kvarstå och inte längre vara en revision.
self.assertTrue(paragraphs[1].is_move_from_revision)
# "Move to"-revisionen är det stycke där vi drog texten till.
# Om vi avvisar revisionen kommer detta stycke istället att försvinna, och det andra kommer att kvarstå.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

