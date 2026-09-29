---
title: Comment.story_type property
linktitle: story_type property
articleTitle: story_type property
second_title: Aspose.Words for Python
description: "Comment.story_type property. Returns [StoryType.COMMENTS](../../storytype/#COMMENTS)."
type: docs
weight: 120
url: /it/python-net/aspose.words/comment/story_type/
---

## Comment.story_type property

Returns [StoryType.COMMENTS](../../storytype/#COMMENTS).



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
# I nodi Table hanno un metodo "EnsureMinimum()" che garantisce che la tabella abbia almeno una cella.
table = aw.tables.Table(doc)
table.ensure_minimum()
# Possiamo inserire una tabella all'interno di una nota a piè di pagina, facendo sì che appaia nel piè di pagina della pagina di riferimento.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# Anche InlineStory dispone di un metodo "EnsureMinimum()", ma in questo caso,
# assicura che l'ultimo figlio del nodo sia un paragrafo,
# per permetterci di fare clic e scrivere testo facilmente in Microsoft Word.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# Modifica l'aspetto dell'ancora, che è il piccolo numero in apice
# nel testo principale che punta alla nota a piè di pagina.
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# Tutti i nodi di storia inline hanno i rispettivi tipi di storia.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# Un commento è un altro tipo di storia inline.
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# Il paragrafo genitore di un nodo di storia inline sarà quello del corpo principale del documento.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# Tuttavia, l'ultimo paragrafo è quello del contenuto testuale del commento,
# che sarà al di fuori del corpo principale del documento in un fumetto.
# Un commento non avrà alcun nodo figlio per impostazione predefinita,
# quindi possiamo applicare il metodo EnsureMinimum() per inserire anche qui un paragrafo.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# Una volta che abbiamo un paragrafo, possiamo spostare il builder per farlo e scrivere il nostro commento.
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words](../../)
* class [Comment](../)

