---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /sv/python-net/aspose.words/documentbuilder/move_to/
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
# Skapa ett giltigt bokmärke, en entitet som består av noder omslutna av en bokmärkesstartnod,
# och en bokmärkesslutnod.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# Dokumentbyggarens markör är alltid framför den nod vi senast lade till med den.
# Om byggarens markör är i slutet av dokumentet kommer dess aktuella nod att vara null.
# Den föregående noden är bokmärkesslutnoden som vi senast lade till.
# Att lägga till nya noder med byggaren kommer att fästa dem efter den sista noden.
self.assertIsNone(builder.current_node)
# Om vi vill redigera en annan del av dokumentet med byggaren,
# behöver vi flytta dess markör till den nod vi vill redigera.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# Att flytta den till ett bokmärke kommer att flytta den till den första noden inom bokmärkesstart- och slutnoderna, den omslutna körningen.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# Vi kan också flytta markören till en enskild nod på detta sätt.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# Vi kan använda specifika metoder för att flytta till början/slutet av ett dokument.
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
# Dokumentbyggaren har en markör, som fungerar som delen av dokumentet
# där byggaren lägger till nya noder när vi använder dess dokumentkonstruktionsmetoder.
# Denna markör fungerar på samma sätt som Microsoft Words blinkande markör,
# och den hamnar också alltid omedelbart efter varje nod som byggaren just infogat.
# För att lägga till innehåll i en annan del av dokumentet,
# kan vi flytta markören till en annan nod med "MoveTo"-metoden.
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Markören är nu framför den nod vi flyttade den till.
# Att lägga till ett andra textstycke kommer att infoga det framför det första textstycket.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Flytta markören till slutet av dokumentet för att fortsätta lägga till text i slutet som tidigare.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

