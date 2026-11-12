---
title: NodeCollection indexer
linktitle: NodeCollection indexer
articleTitle: NodeCollection indexer
second_title: Aspose.Words for Python
description: "NodeCollection indexer. Retrieves a node at the given index."
type: docs
weight: 10
url: /ru/python-net/aspose.words/nodecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a node at the given index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to traverse through a composite node's collection of child nodes.

```python
doc = aw.Document()
# Добавьте два текста (run) и одну форму в качестве дочерних узлов к первому абзацу этого документа.
paragraph = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
paragraph.append_child(aw.Run(doc=doc, text='Hello world! '))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 200
shape.height = 200
# Обратите внимание, что 'CustomNodeId' не сохраняется в выходной файл и существует только в течение жизненного цикла узла.
shape.custom_node_id = 100
shape.wrap_type = aw.drawing.WrapType.INLINE
paragraph.append_child(shape)
paragraph.append_child(aw.Run(doc=doc, text='Hello again!'))
# Итерировать коллекцию непосредственных дочерних элементов абзаца,
# и вывести любые последовательности текста или фигуры, которые мы найдём внутри.
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
* class [NodeCollection](../)

