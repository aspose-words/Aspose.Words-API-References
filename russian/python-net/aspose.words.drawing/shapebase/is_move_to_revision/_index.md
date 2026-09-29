---
title: ShapeBase.is_move_to_revision property
linktitle: is_move_to_revision property
articleTitle: is_move_to_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_to_revision property. Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 350
url: /ru/python-net/aspose.words.drawing/shapebase/is_move_to_revision/
---

## ShapeBase.is_move_to_revision property

Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.



```python
@property
def is_move_to_revision(self) -> bool:
    ...

```

### Examples

Shows how to identify move revision shapes.

```python
# Перемещение‑ревизия происходит, когда мы перемещаем элемент в теле документа с помощью вырезания и вставки в Microsoft Word, при этом
# отслеживании изменений. Если в такое перемещение текста включить встроенную фигуру, эта фигура также станет ревизией.
# Копирование и вставка или перемещение плавающих фигур не создают перемещения‑ревизий.
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# Перемещения‑ревизии состоят из пар ревизий "Move from" и "Move to". Мы переместили в этом документе одну фигуру,
# но пока мы не примем или не отклоним перемещение‑ревизию, будет две копии этой фигуры.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Это ревизия "Move to", которая является фигурой в её конечном месте назначения.
# Если мы примем ревизию, эта фигура ревизии "Move to" исчезнет,
# а фигура ревизии "Move from" останется.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# Это ревизия "Move from", которая является фигурой в её исходном месте.
# Если мы примем ревизию, эта фигура ревизии "Move from" исчезнет,
# а фигура ревизии "Move to" останется.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

