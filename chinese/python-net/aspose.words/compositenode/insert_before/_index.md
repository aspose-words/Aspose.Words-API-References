---
title: CompositeNode.insert_before method
linktitle: insert_before method
articleTitle: insert_before method
second_title: Aspose.Words for Python
description: "CompositeNode.insert_before method. Inserts the specified node immediately before the specified reference node."
type: docs
weight: 140
url: /zh/python-net/aspose.words/compositenode/insert_before/
---

## insert_before(new_child, ref_child) {#node_node}

Inserts the specified node immediately before the specified reference node.


```python
def insert_before(self, new_child: aspose.words.Node, ref_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The [Node](../../node/) to insert. |
| ref_child | [Node](../../node/) | The [Node](../../node/) that is the reference node. The *newChild* is placed before this node. |

### Remarks

If *refChild* is``None``, inserts *newChild* at the end of the list of child nodes.




If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The inserted node.


### Examples

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

