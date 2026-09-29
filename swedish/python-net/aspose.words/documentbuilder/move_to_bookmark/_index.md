---
title: DocumentBuilder.move_to_bookmark method
linktitle: move_to_bookmark method
articleTitle: move_to_bookmark method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_bookmark method"
type: docs
weight: 530
url: /sv/python-net/aspose.words/documentbuilder/move_to_bookmark/
---

## move_to_bookmark(bookmark_name) {#str}

Moves the cursor to a bookmark.


```python
def move_to_bookmark(self, bookmark_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str | The name of the bookmark to move the cursor to. |

### Remarks

Moves the cursor to a position just after the start of the bookmark with the
specified name.

The comparison is not case-sensitive. If the bookmark was not found, ``False`` is
returned and the cursor is not moved.

Inserting new text does not replace existing text of the bookmark.

Note that some bookmarks in the document are assigned to form fields.
Moving to such a bookmark and inserting text there inserts the text into the
form field code. Although this will not invalidate the form field, the inserted
text will not be visible because it becomes part of the field code.




### Returns

``True`` if the bookmark was found; ``False`` otherwise.


## move_to_bookmark(bookmark_name, is_start, is_after) {#str_bool_bool}

Moves the cursor to a bookmark with greater precision.


```python
def move_to_bookmark(self, bookmark_name: str, is_start: bool, is_after: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str | The name of the bookmark to move the cursor to. |
| is_start | bool | When ``True``, moves the cursor to the beginning of the bookmark. When ``False``, moves the cursor to the end of the bookmark. |
| is_after | bool | When ``True``, moves the cursor to be after the bookmark start or end position. When ``False``, moves the cursor to be before the bookmark start or end position. |

### Remarks

Moves the cursor to a position before or after the bookmark start or end.

If desired position is not at inline level, moves to the next paragraph.

The comparison is not case-sensitive. If the bookmark was not found, ``False`` is
returned and the cursor is not moved.




### Returns

``True`` if the bookmark was found; ``False`` otherwise.


## Examples

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

Shows how to move a document builder's node insertion point cursor to a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ett giltigt bokmärke består av en BookmarkStart-nod, en BookmarkEnd-nod med en
# matchande bokmärkesnamn någonstans efteråt, och innehåll som omsluts av dessa noder.
builder.start_bookmark('MyBookmark')
builder.write('Hello world! ')
builder.end_bookmark('MyBookmark')
# Det finns 4 sätt att flytta en dokumentbyggares markör till ett bokmärke.
# Om vi befinner oss mellan BookmarkStart- och BookmarkEnd-noderna kommer markören att vara inne i bokmärket.
# Detta betyder att all text som läggs till av byggaren blir en del av bokmärket.
# 1 -  Utanför bokmärket, framför BookmarkStart-noden:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=True, is_after=False))
builder.write('1. ')
self.assertEqual('Hello world! ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. Hello world!', doc.get_text().strip())
# 2 -  Inuti bokmärket, precis efter BookmarkStart-noden:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=True, is_after=True))
builder.write('2. ')
self.assertEqual('2. Hello world! ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world!', doc.get_text().strip())
# 2 -  Inuti bokmärket, precis framför BookmarkEnd-noden:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=False, is_after=False))
builder.write('3. ')
self.assertEqual('2. Hello world! 3. ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world! 3.', doc.get_text().strip())
# 4 -  Utanför bokmärket, efter BookmarkEnd-noden:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=False, is_after=True))
builder.write('4.')
self.assertEqual('2. Hello world! 3. ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world! 3. 4.', doc.get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

