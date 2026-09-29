---
title: Footnote.story_type property
linktitle: story_type property
articleTitle: story_type property
second_title: Aspose.Words for Python
description: "Footnote.story_type property. Returns [StoryType.FOOTNOTES](../../../aspose.words/storytype/#FOOTNOTES) or [StoryType.ENDNOTES](../../../aspose.words/storytype/#ENDNOTES)."
type: docs
weight: 70
url: /sv/python-net/aspose.words.notes/footnote/story_type/
---

## Footnote.story_type property

Returns [StoryType.FOOTNOTES](../../../aspose.words/storytype/#FOOTNOTES) or [StoryType.ENDNOTES](../../../aspose.words/storytype/#ENDNOTES).



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
# Tabellnoder har en "EnsureMinimum()"-metod som säkerställer att tabellen har minst en cell.
table = aw.tables.Table(doc)
table.ensure_minimum()
# Vi kan placera en tabell i en fotnot, vilket får den att visas i sidfoten på den refererande sidan.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# En InlineStory har också en "EnsureMinimum()"-metod, men i det här fallet,
# säkerställer att den sista barnet till noden är ett stycke,
# så att vi kan klicka och skriva text enkelt i Microsoft Word.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# Redigera utseendet på ankaret, som är den lilla upphöjda siffran
# i huvudtexten som pekar på fotnoten.
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# Alla inline‑story‑noder har sina respektive story‑typer.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# En kommentar är en annan typ av inline‑story.
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# Föräldra‑stycket för en inline‑story‑nod kommer att vara det från huvuddokumentets kropp.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# Dock är det sista stycket det från kommentarens textinnehåll,
# vilket kommer att ligga utanför huvuddokumentets kropp i en pratbubbla.
# En kommentar har som standard inga barnnoder,
# så vi kan använda EnsureMinimum()-metoden för att placera ett stycke här också.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# När vi har ett stycke kan vi flytta byggaren för att göra det och skriva vår kommentar.
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)

