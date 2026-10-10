---
title: CompositeNode.get_child_nodes method
linktitle: get_child_nodes method
articleTitle: get_child_nodes method
second_title: Aspose.Words for Python
description: "CompositeNode.get_child_nodes method. Returns a live collection of child nodes that match the specified type."
type: docs
weight: 100
url: /zh/python-net/aspose.words/compositenode/get_child_nodes/
---

## get_child_nodes(node_type, is_deep) {#nodetype_bool}

Returns a live collection of child nodes that match the specified type.


```python
def get_child_nodes(self, node_type: aspose.words.NodeType, is_deep: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node_type | [NodeType](../../nodetype/) | Specifies the type of nodes to select. |
| is_deep | bool | ``True`` to select from all child nodes recursively; ``False`` to select only among immediate children.  |

### Remarks

The collection of nodes returned by this method is always live.




A live collection is always in sync with the document. For example, if you
selected all sections in a document and enumerate through the collection
deleting the sections, the section is removed from the collection immediately
when it is removed from the document.




### Returns

A live collection of child nodes of the specified type.


### Examples

Shows how to print all of a document's comments and their replies.

```python
doc = aw.Document(file_name=MY_DIR + 'Comments.docx')
comments = doc.get_child_nodes(aw.NodeType.COMMENT, True)
# 如果评论没有祖先，它就是一个“顶级”评论，而不是回复类型的评论。
# 打印所有顶级评论以及它们可能拥有的任何回复。
for comment in list(filter(lambda c: c.ancestor == None, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_comment(), b), list(comments)))))):
    print('Top-level comment:')
    print(f'\t"{comment.get_text().strip()}", by {comment.author}')
    print(f'Has {comment.replies.count} replies')
    for comment_reply in comment.replies:
        comment_reply = comment_reply.as_comment()
        print(f'\t"{comment_reply.get_text().strip()}", by {comment_reply.author}')
    print()
```

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()
# 向本文档的第一段添加两个运行（run）和一个形状作为子节点。
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc=doc, text='Hello world! '))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# 请注意，'CustomNodeId' 不会保存到输出文件中，仅在节点生命周期内存在。
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)
paragraph.append_child(aw.Run(doc=doc, text='Hello again!'))
# 遍历段落的直接子项集合，
# 并打印我们在其中找到的任何运行或形状。
children = paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, False).count)
for child in children:
    switch_condition = child.node_type
    if switch_condition == aw.NodeType.RUN:
        print('Run contents:')
        print(f'\t"{child.get_text().strip()}"')
    elif switch_condition == aw.NodeType.SHAPE:
        child_shape = child.as_shape()
        print('Shape:')
        print(f'\t{child_shape.shape_type}, {child_shape.width}x{child_shape.height}')
```

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()
# 空文档默认包含一个段落。
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# 复合节点（例如我们的段落）可以包含其他复合节点和内联节点作为子节点。
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc=doc, text='Initial text. ')
paragraph.append_child(paragraph_text)
# 创建另外三个运行节点。
run1 = aw.Run(doc=doc, text='Run 1. ')
run2 = aw.Run(doc=doc, text='Run 2. ')
run3 = aw.Run(doc=doc, text='Run 3. ')
# 文档主体在我们将这些运行插入到复合节点之前不会显示它们
# 该节点本身是文档节点树的一部分，就像我们对第一个运行所做的那样。
# 我们可以确定插入的节点的文本内容位于何处
# 通过相对于段落中另一个节点指定插入位置，来决定它在文档中的出现位置。
self.assertEqual('Initial text.', paragraph.get_text().strip())
# 将第二个运行插入段落中，位于初始运行之前。
paragraph.insert_before(run2, paragraph_text)
self.assertEqual('Run 2. Initial text.', paragraph.get_text().strip())
# 将第三个运行插入初始运行之后。
paragraph.insert_after(run3, paragraph_text)
self.assertEqual('Run 2. Initial text. Run 3.', paragraph.get_text().strip())
# 将第一个运行插入到段落子节点集合的开头。
paragraph.prepend_child(run1)
self.assertEqual('Run 1. Run 2. Initial text. Run 3.', paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
# 我们可以通过编辑和删除现有子节点来修改运行的内容。
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = 'Updated run 2. '
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)
self.assertEqual('Run 1. Updated run 2. Run 3.', paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

