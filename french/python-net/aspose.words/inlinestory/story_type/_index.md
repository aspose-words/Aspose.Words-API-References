---
title: InlineStory.story_type property
linktitle: story_type property
articleTitle: story_type property
second_title: Aspose.Words for Python
description: "InlineStory.story_type property. Returns the type of the story."
type: docs
weight: 100
url: /fr/python-net/aspose.words/inlinestory/story_type/
---

## InlineStory.story_type property

Returns the type of the story.


```python
@property
def story_type(self) -> aspose.words.StoryType:
    ...

```

### Examples

Shows how to insert InlineStory nodes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=None)
# Les nœuds Table possèdent une méthode "EnsureMinimum()" qui garantit que le tableau possède au moins une cellule.
table = aw.tables.Table(doc)
table.ensure_minimum()
# Nous pouvons placer un tableau dans une note de bas de page, ce qui le fera apparaître dans le pied de page de la page de référence.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# Un InlineStory possède également une méthode "EnsureMinimum()", mais dans ce cas,
# elle s'assure que le dernier enfant du nœud est un paragraphe,
# pour que nous puissions cliquer et saisir du texte facilement dans Microsoft Word.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# Modifiez l'apparence de l'ancre, qui est le petit chiffre en exposant
# dans le texte principal qui pointe vers la note de bas de page.
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# Tous les nœuds d'histoire en ligne ont leurs types d'histoire respectifs.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# Un commentaire est un autre type d'histoire en ligne.
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# Le paragraphe parent d'un nœud d'histoire en ligne sera celui du corps principal du document.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# Cependant, le dernier paragraphe est celui du contenu texte du commentaire,
# qui sera en dehors du corps principal du document dans une bulle de dialogue.
# Un commentaire n'aura aucun nœud enfant par défaut,
# nous pouvons donc appliquer la méthode EnsureMinimum() pour placer un paragraphe ici également.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# Une fois que nous avons un paragraphe, nous pouvons déplacer le constructeur pour le faire et écrire notre commentaire.
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

