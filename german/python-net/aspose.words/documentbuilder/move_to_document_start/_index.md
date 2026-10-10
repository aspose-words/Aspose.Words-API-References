---
title: DocumentBuilder.move_to_document_start method
linktitle: move_to_document_start method
articleTitle: move_to_document_start method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_document_start method. Moves the cursor to the beginning of the document."
type: docs
weight: 560
url: /de/python-net/aspose.words/documentbuilder/move_to_document_start/
---

## move_to_document_start() {#default}

Moves the cursor to the beginning of the document.


```python
def move_to_document_start(self):
    ...
```

### Examples

Shows how to move a document builder's cursor to different nodes in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstelle ein gültiges Lesezeichen, ein Objekt, das aus Knoten besteht, die von einem Lesezeichen-Startknoten umschlossen werden,
# und einem Lesezeichen-Endknoten.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# Der Cursor des Dokument-Builders steht immer vor dem Knoten, den wir zuletzt damit hinzugefügt haben.
# Wenn der Cursor des Builders am Ende des Dokuments ist, wird sein aktueller Knoten null sein.
# Der vorherige Knoten ist der Lesezeichen-Endknoten, den wir zuletzt hinzugefügt haben.
# Das Hinzufügen neuer Knoten mit dem Builder wird sie an den letzten Knoten anhängen.
self.assertIsNone(builder.current_node)
# Wenn wir mit dem Builder einen anderen Teil des Dokuments bearbeiten möchten,
# müssen wir seinen Cursor zu dem Knoten bringen, den wir bearbeiten wollen.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# Das Verschieben zu einem Lesezeichen bewegt ihn zum ersten Knoten innerhalb der Lesezeichen-Start- und Endknoten, dem eingeschlossenen Lauf.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# Wir können den Cursor auch zu einem einzelnen Knoten wie folgt bewegen.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# Wir können spezifische Methoden verwenden, um zum Anfang/Ende eines Dokuments zu springen.
builder.move_to_document_end()
self.assertTrue(builder.is_at_end_of_paragraph)
builder.move_to_document_start()
self.assertTrue(builder.is_at_start_of_paragraph)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

