---
title: InlineStory.tables property
linktitle: tables property
articleTitle: tables property
second_title: Aspose.Words for Python
description: "InlineStory.tables property. Gets a collection of tables that are immediate children of the story."
type: docs
weight: 110
url: /de/python-net/aspose.words/inlinestory/tables/
---

## InlineStory.tables property

Gets a collection of tables that are immediate children of the story.


```python
@property
def tables(self) -> aspose.words.tables.TableCollection:
    ...

```

### Examples

Shows how to insert InlineStory nodes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
footnote = builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=None)
# Tabellenknoten besitzen eine "EnsureMinimum()"-Methode, die sicherstellt, dass die Tabelle mindestens eine Zelle enthält.
table = aw.tables.Table(doc)
table.ensure_minimum()
# Wir können eine Tabelle in einer Fußnote platzieren, wodurch sie in der Fußzeile der referenzierenden Seite erscheint.
self.assertEqual(0, footnote.tables.count)
footnote.append_child(table)
self.assertEqual(1, footnote.tables.count)
self.assertEqual(aw.NodeType.TABLE, footnote.last_child.node_type)
# Ein InlineStory verfügt ebenfalls über eine "EnsureMinimum()"-Methode, jedoch in diesem Fall,
# stellt sie sicher, dass das letzte Kind des Knotens ein Absatz ist,
# damit wir in Microsoft Word leicht klicken und Text schreiben können.
footnote.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, footnote.last_child.node_type)
# Bearbeiten Sie das Aussehen des Ankers, der die kleine hochgestellte Zahl ist
# im Haupttext, der auf die Fußnote verweist.
footnote.font.name = 'Arial'
footnote.font.color = aspose.pydrawing.Color.green
# Alle Inline-Story-Knoten haben ihre jeweiligen Story-Typen.
self.assertEqual(aw.StoryType.FOOTNOTES, footnote.story_type)
# Ein Kommentar ist ein weiterer Typ einer Inline-Story.
comment = builder.current_paragraph.append_child(aw.Comment(doc=doc, author='John Doe', initial='J. D.', date_time=datetime.datetime.now())).as_comment()
# Der übergeordnete Absatz eines Inline-Story-Knotens stammt aus dem Hauptdokumentkörper.
self.assertEqual(doc.first_section.body.first_paragraph, comment.parent_paragraph)
# Allerdings ist der letzte Absatz derjenige aus dem Kommentartextinhalt,
# der außerhalb des Hauptdokumentkörpers in einer Sprechblase angezeigt wird.
# Ein Kommentar hat standardmäßig keine Kindknoten,
# so können wir die EnsureMinimum()-Methode anwenden, um hier ebenfalls einen Absatz einzufügen.
self.assertIsNone(comment.last_paragraph)
comment.ensure_minimum()
self.assertEqual(aw.NodeType.PARAGRAPH, comment.last_child.node_type)
# Sobald wir einen Absatz haben, können wir den Builder verschieben, um ihn zu erstellen, und unseren Kommentar schreiben.
builder.move_to(comment.last_paragraph)
builder.write('My comment.')
self.assertEqual(aw.StoryType.COMMENTS, comment.story_type)
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.InsertInlineStoryNodes.docx')
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

