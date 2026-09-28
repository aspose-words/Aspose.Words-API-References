---
title: ShapeBase.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 340
url: /zh/python-net/aspose.words.drawing/shapebase/is_move_from_revision/
---

## ShapeBase.is_move_from_revision property

Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_from_revision(self) -> bool:
    ...

```

### Examples

Shows how to identify move revision shapes.

```python
# 移动修订是指我们在 Microsoft Word 中通过剪切粘贴移动文档正文中的元素时，
# 并跟踪更改。如果在此类文本移动中涉及内联形状，该形状也将成为修订。
# 复制粘贴或移动浮动形状不会创建移动修订。
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# 移动修订由 "Move from" 与 "Move to" 成对的修订组成。我们在此文档中移动了一个形状，
# 但在接受或拒绝该移动修订之前，该形状将会出现两个实例。
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# 这是 "Move to" 修订，它是位于到达目的地的形状。
# 如果我们接受此修订，这个 "Move to" 修订形状将会消失，
# 并且 "Move from" 修订形状将会保留。
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# 这是 "Move from" 修订，它是位于原始位置的形状。
# 如果我们接受此修订，这个 "Move from" 修订形状将会消失，
# 并且 "Move to" 修订形状将会保留。
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

