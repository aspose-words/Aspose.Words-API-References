---
title: DocumentBuilder.move_to_bookmark method
linktitle: move_to_bookmark method
articleTitle: move_to_bookmark method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_bookmark method"
type: docs
weight: 530
url: /ru/python-net/aspose.words/documentbuilder/move_to_bookmark/
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
# Создать действительную закладку, объект, состоящий из узлов, заключённых между начальным узлом закладки,
# и конечным узлом закладки.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# Курсор построителя документа всегда находится впереди узла, который мы последним добавили с его помощью.
# Если курсор построителя находится в конце документа, его текущий узел будет равен null.
# Предыдущий узел — это конечный узел закладки, который мы последним добавили.
# Добавление новых узлов с помощью построителя присоединит их к последнему узлу.
self.assertIsNone(builder.current_node)
# Если мы хотим отредактировать другую часть документа с помощью построителя,
# нам потребуется переместить его курсор к узлу, который мы хотим отредактировать.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# Перемещение его к закладке переместит его к первому узлу внутри начального и конечного узлов закладки, заключённому фрагменту.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# Мы также можем переместить курсор к отдельному узлу следующим образом.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# Мы можем использовать специальные методы для перемещения к началу/концу документа.
builder.move_to_document_end()
self.assertTrue(builder.is_at_end_of_paragraph)
builder.move_to_document_start()
self.assertTrue(builder.is_at_start_of_paragraph)
```

Shows how to move a document builder's node insertion point cursor to a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Допустимая закладка состоит из узла BookmarkStart, узла BookmarkEnd с
# соответствующим именем закладки где‑то позже и содержимым, заключённым между этими узлами.
builder.start_bookmark('MyBookmark')
builder.write('Hello world! ')
builder.end_bookmark('MyBookmark')
# Существует 4 способа перемещения курсора построителя документа к закладке.
# Если мы находимся между узлами BookmarkStart и BookmarkEnd, курсор будет внутри закладки.
# Это означает, что любой текст, добавленный построителем, станет частью закладки.
# 1 -  Вне закладки, перед узлом BookmarkStart:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=True, is_after=False))
builder.write('1. ')
self.assertEqual('Hello world! ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. Hello world!', doc.get_text().strip())
# 2 -  Внутри закладки, сразу после узла BookmarkStart:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=True, is_after=True))
builder.write('2. ')
self.assertEqual('2. Hello world! ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world!', doc.get_text().strip())
# 2 -  Внутри закладки, непосредственно перед узлом BookmarkEnd:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=False, is_after=False))
builder.write('3. ')
self.assertEqual('2. Hello world! 3. ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world! 3.', doc.get_text().strip())
# 4 -  Вне закладки, после узла BookmarkEnd:
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=False, is_after=True))
builder.write('4.')
self.assertEqual('2. Hello world! 3. ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world! 3. 4.', doc.get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

