---
title: Node.custom_node_id property
linktitle: custom_node_id property
articleTitle: custom_node_id property
second_title: Aspose.Words for Python
description: "Node.custom_node_id property. Specifies custom node identifier."
type: docs
weight: 10
url: /zh/python-net/aspose.words/node/custom_node_id/
---

## Node.custom_node_id property

Specifies custom node identifier.


```python
@property
def custom_node_id(self) -> int:
    ...

@custom_node_id.setter
def custom_node_id(self, value: int):
    ...

```

### Remarks

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.




### Examples

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

### See Also

* module [aspose.words](../../)
* class [Node](../)

