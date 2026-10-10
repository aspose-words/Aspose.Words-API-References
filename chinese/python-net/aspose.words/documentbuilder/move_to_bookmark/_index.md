---
title: DocumentBuilder.move_to_bookmark method
linktitle: move_to_bookmark method
articleTitle: move_to_bookmark method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.move_to_bookmark method"
type: docs
weight: 530
url: /zh/python-net/aspose.words/documentbuilder/move_to_bookmark/
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
# 创建一个有效的书签，它是由书签开始节点和书签结束节点之间的节点组成的实体，
# 以及书签结束节点。
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# 文档生成器的光标始终位于我们上次使用它添加的节点之前。
# 如果生成器的光标位于文档末尾，则其当前节点将为 null。
# 前一个节点是我们上次添加的书签结束节点。
# 使用生成器添加新节点会将它们附加到最后一个节点。
self.assertIsNone(builder.current_node)
# 如果我们希望使用生成器编辑文档的其他部分，
# 我们需要将其光标移动到想要编辑的节点。
builder.move_to_bookmark(bookmark_name='MyBookmark')
# 将光标移动到书签会将其定位到书签开始和结束节点之间的第一个节点，即包含的运行。
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# 我们也可以这样将光标移动到单个节点。
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# 我们可以使用特定的方法移动到文档的开始/结束位置。
builder.move_to_document_end()
self.assertTrue(builder.is_at_end_of_paragraph)
builder.move_to_document_start()
self.assertTrue(builder.is_at_start_of_paragraph)
```

Shows how to move a document builder's node insertion point cursor to a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 有效的书签由一个 BookmarkStart 节点、一个带有
# 匹配书签名称的后续节点以及这些节点之间包裹的内容组成。
builder.start_bookmark('MyBookmark')
builder.write('Hello world! ')
builder.end_bookmark('MyBookmark')
# 将文档生成器的光标移动到书签有 4 种方式。
# 如果我们位于 BookmarkStart 和 BookmarkEnd 节点之间，光标将位于书签内部。
# 这意味着生成器添加的任何文本都将成为书签的一部分。
# 1 -  在书签外部，位于 BookmarkStart 节点之前：
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=True, is_after=False))
builder.write('1. ')
self.assertEqual('Hello world! ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. Hello world!', doc.get_text().strip())
# 2 -  在书签内部，紧跟在 BookmarkStart 节点之后：
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=True, is_after=True))
builder.write('2. ')
self.assertEqual('2. Hello world! ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world!', doc.get_text().strip())
# 2 -  在书签内部，紧靠 BookmarkEnd 节点之前：
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=False, is_after=False))
builder.write('3. ')
self.assertEqual('2. Hello world! 3. ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world! 3.', doc.get_text().strip())
# 4 -  在书签外部，位于 BookmarkEnd 节点之后：
self.assertTrue(builder.move_to_bookmark(bookmark_name='MyBookmark', is_start=False, is_after=True))
builder.write('4.')
self.assertEqual('2. Hello world! 3. ', doc.range.bookmarks.get_by_name('MyBookmark').text)
self.assertEqual('1. 2. Hello world! 3. 4.', doc.get_text().strip())
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

