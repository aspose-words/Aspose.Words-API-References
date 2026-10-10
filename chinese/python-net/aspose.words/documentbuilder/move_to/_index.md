---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /zh/python-net/aspose.words/documentbuilder/move_to/
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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# 文档构建器有一个光标，它充当文档的部分
# 当我们使用其文档构建方法时，构建器在此处追加新节点。
# 此光标的功能与 Microsoft Word 的闪烁光标相同，
# 并且它总是位于构建器刚插入的任何节点之后紧接位置。
# 要将内容追加到文档的其他部分，
# 我们可以使用 "MoveTo" 方法将光标移动到另一个节点。
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# 光标现在位于我们移动到的节点前面。
# 添加第二个运行将把它插入到第一个运行之前。
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# 将光标移动到文档末尾，以继续像以前一样在末尾追加文本。
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

