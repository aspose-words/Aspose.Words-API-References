---
title: Story.paragraphs property
linktitle: paragraphs property
articleTitle: paragraphs property
second_title: Aspose.Words for Python
description: "Story.paragraphs property. Gets a collection of paragraphs that are immediate children of the story."
type: docs
weight: 30
url: /fr/python-net/aspose.words/story/paragraphs/
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
# Ce document contient des révisions "Move", qui apparaissent lorsque nous sélectionnons du texte avec le curseur,
# et le faisons ensuite glisser pour le déplacer vers un autre emplacement
# tout en suivant les révisions dans Microsoft Word via "Review" -> "Track changes".
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Les révisions de déplacement se composent de paires de révisions "Move from" et "Move to".
# Ces révisions sont des modifications potentielles du document que nous pouvons soit accepter, soit rejeter.
# Avant d'accepter/rejeter une révision de déplacement, le document
# doit garder une trace à la fois des destinations de départ et d'arrivée du texte.
# Le deuxième et le quatrième paragraphe définissent une telle révision, et donc les deux ont le même contenu.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# La révision "Move from" est le paragraphe d'où nous avons fait glisser le texte.
# Si nous acceptons la révision, ce paragraphe disparaîtra,
# et l'autre restera et ne sera plus une révision.
self.assertTrue(paragraphs[1].is_move_from_revision)
# La révision "Move to" est le paragraphe où nous avons fait glisser le texte.
# Si nous rejetons la révision, ce paragraphe disparaîtra à la place, et l'autre restera.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

