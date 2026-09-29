---
title: DocumentBuilder.move_to_document_end method
linktitle: move_to_document_end method
articleTitle: move_to_document_end method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to_document_end method. Moves the cursor to the end of the document."
type: docs
weight: 550
url: /sv/python-net/aspose.words/documentbuilder/move_to_document_end/
---

## move_to_document_end() {#default}

Moves the cursor to the end of the document.


```python
def move_to_document_end(self):
    ...
```

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

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

