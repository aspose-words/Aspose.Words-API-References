---
title: ShapeBase.is_move_from_revision property
linktitle: is_move_from_revision property
articleTitle: is_move_from_revision property
second_title: Aspose.Words for Python
description: "ShapeBase.is_move_from_revision property. Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled."
type: docs
weight: 340
url: /tr/python-net/aspose.words.drawing/shapebase/is_move_from_revision/
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
# Taşıma revizyonu, Microsoft Word'de bir öğeyi kesip yapıştırarak belge gövdesinde hareket ettirdiğimizde ortaya çıkar
# değişiklikleri izlerken. Böyle bir metin hareketine satır içi bir şekil dahil edersek, o şekil de bir revizyon olur.
# Kopyala-yapıştır veya yüzen şekilleri taşıma, taşıma revizyonları oluşturmaz.
doc = aw.Document(file_name=MY_DIR + 'Revision shape.docx')
# "Move from" ve "Move to" revizyon çiftlerinden oluşur. Bu belgede bir şekil içinde taşıma yaptık,
# ancak taşıma revizyonunu kabul edip reddedene kadar, o şeklin iki örneği olacaktır.
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(2, len(shapes))
# Bu, "Move to" revizyonudur, bu şekil varış noktasındaki halidir.
# Revizyonu kabul edersek, bu "Move to" revizyon şekli kaybolacak,
# ve "Move from" revizyon şekli kalacaktır.
self.assertFalse(shapes[0].is_move_from_revision)
self.assertTrue(shapes[0].is_move_to_revision)
# Bu, "Move from" revizyonudur, bu şekil orijinal konumundadır.
# Revizyonu kabul edersek, bu "Move from" revizyon şekli kaybolacak,
# ve "Move to" revizyon şekli kalacaktır.
self.assertTrue(shapes[1].is_move_from_revision)
self.assertFalse(shapes[1].is_move_to_revision)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

