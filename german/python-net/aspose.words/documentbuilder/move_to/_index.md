---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /de/python-net/aspose.words/documentbuilder/move_to/
---

## move_to(node) {#node}

Moves the cursor to an inline node or to the end of a paragraph.


```python
def move_to(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node must be a paragraph or a direct child of a paragraph. |

### Remarks

When *node* is an inline-level node, the cursor is moved to this node
and further content will be inserted before that node.

When *node* is a [Paragraph](../../paragraph/), the cursor is moved to the end of the paragraph
and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node
and further content will be inserted just before the paragraph break.




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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# Der Dokumenten-Builder hat einen Cursor, der als Teil des Dokuments fungiert
# wo der Builder neue Knoten anhängt, wenn wir seine Dokumentenkonstruktionsmethoden verwenden.
# Dieser Cursor funktioniert auf die gleiche Weise wie der blinkende Cursor von Microsoft Word,
# und er endet außerdem immer unmittelbar nach jedem Knoten, den der Builder gerade eingefügt hat.
# Um Inhalt an einem anderen Teil des Dokuments anzuhängen,
# können wir den Cursor mit der Methode "MoveTo" zu einem anderen Knoten bewegen.
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Der Cursor befindet sich jetzt vor dem Knoten, zu dem wir ihn bewegt haben.
# Das Hinzufügen eines zweiten Laufs wird ihn vor dem ersten Lauf einfügen.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Bewegen Sie den Cursor ans Ende des Dokuments, um das Anfügen von Text am Ende wie zuvor fortzusetzen.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

