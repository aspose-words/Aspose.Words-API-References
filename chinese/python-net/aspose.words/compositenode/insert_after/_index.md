---
title: CompositeNode.insert_after method
linktitle: insert_after method
articleTitle: insert_after method
second_title: Aspose.Words for Python
description: "CompositeNode.insert_after method. Inserts the specified node immediately after the specified reference node."
type: docs
weight: 130
url: /zh/python-net/aspose.words/compositenode/insert_after/
---

## insert_after(new_child, ref_child) {#node_node}

Inserts the specified node immediately after the specified reference node.


```python
def insert_after(self, new_child: aspose.words.Node, ref_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The [Node](../../node/) to insert. |
| ref_child | [Node](../../node/) | The [Node](../../node/) that is the reference node. The *newChild* is placed after the*refChild*. |

### Remarks

If *refChild* is``None``, inserts *newChild* at the beginning of the list of child nodes.




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

Shows how to replace all textbox shapes with image shapes.

```python
doc = aw.Document(file_name=MY_DIR + 'Textboxes in drawing canvas.docx')
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(3, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.TEXT_BOX, shapes))))
self.assertEqual(1, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.IMAGE, shapes))))
for shape in shapes:
    if shape.shape_type == aw.drawing.ShapeType.TEXT_BOX:
        replacement_shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
        replacement_shape.image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
        replacement_shape.left = shape.left
        replacement_shape.top = shape.top
        replacement_shape.width = shape.width
        replacement_shape.height = shape.height
        replacement_shape.relative_horizontal_position = shape.relative_horizontal_position
        replacement_shape.relative_vertical_position = shape.relative_vertical_position
        replacement_shape.horizontal_alignment = shape.horizontal_alignment
        replacement_shape.vertical_alignment = shape.vertical_alignment
        replacement_shape.wrap_type = shape.wrap_type
        replacement_shape.wrap_side = shape.wrap_side
        shape.parent_node.insert_after(replacement_shape, shape)
        shape.remove()
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(0, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.TEXT_BOX, shapes))))
self.assertEqual(4, len(list(filter(lambda s: s.shape_type == aw.drawing.ShapeType.IMAGE, shapes))))
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ReplaceTextboxesWithImages.docx')
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

