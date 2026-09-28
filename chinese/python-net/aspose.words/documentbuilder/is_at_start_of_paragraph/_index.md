---
title: DocumentBuilder.is_at_start_of_paragraph property
linktitle: is_at_start_of_paragraph property
articleTitle: is_at_start_of_paragraph property
second_title: Aspose.Words for Python
description: "DocumentBuilder.is_at_start_of_paragraph property. Returns ``True`` if the cursor is at the beginning of the current paragraph (no text before the cursor)."
type: docs
weight: 130
url: /zh/python-net/aspose.words/documentbuilder/is_at_start_of_paragraph/
---

## DocumentBuilder.is_at_start_of_paragraph property

Returns ``True`` if the cursor is at the beginning of the current paragraph (no text before the cursor).



```python
@property
def is_at_start_of_paragraph(self) -> bool:
    ...

```

### Examples

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

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

