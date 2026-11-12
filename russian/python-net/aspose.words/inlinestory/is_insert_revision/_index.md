---
title: InlineStory.is_insert_revision property
linktitle: is_insert_revision property
articleTitle: is_insert_revision property
second_title: Aspose.Words for Python
description: "InlineStory.is_insert_revision property. Returns true if this object was inserted in Microsoft Word while change tracking was enabled."
type: docs
weight: 40
url: /ru/python-net/aspose.words/inlinestory/is_insert_revision/
---

## InlineStory.is_insert_revision property

Returns true if this object was inserted in Microsoft Word while change tracking was enabled.


```python
@property
def is_insert_revision(self) -> bool:
    ...

```

### Examples

Shows how to view revision-related properties of InlineStory nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision footnotes.docx')
# Когда мы редактируем документ при включённой опции "Track Changes", доступной через Review -> Tracking,
# включена в Microsoft Word, изменения, которые мы вносим, считаются правками.
# При редактировании документа с использованием Aspose.Words мы можем начать отслеживание правок, вызвав
# вызов метода документа "StartTrackRevisions" и прекратить отслеживание, используя метод "StopTrackRevisions".
# Мы можем либо принять правки, чтобы интегрировать их в документ
# или отклонить их, чтобы отменить и избавиться от предложенного изменения.
self.assertTrue(doc.has_revisions)
footnotes = list(map(lambda x: x.as_footnote(), list(doc.get_child_nodes(aw.NodeType.FOOTNOTE, True))))
self.assertEqual(5, len(footnotes))
# Ниже перечислены пять типов правок, которые могут пометить узел InlineStory.
# 1 -  Правка "insert":
# Эта правка возникает, когда мы вставляем текст при отслеживании изменений.
self.assertTrue(footnotes[2].is_insert_revision)
# 2 -  Правка "move from":
# Когда мы выделяем текст в Microsoft Word и затем перетаскиваем его в другое место в документе
# при отслеживании изменений появляются две правки.
# Правка "move from" представляет собой копию исходного текста до его перемещения.
self.assertTrue(footnotes[4].is_move_from_revision)
# 3 -  Правка "move to":
# Правка "move to" — это текст, который мы переместили в его новое положение в документе.
# "Move from" и "move to" правки появляются парами для каждого перемещения, которое мы выполняем.
# Принятие перемещения удаляет правку "move from" и её текст,
# и сохраняет текст из правки "move to".
# Отклонение перемещения, наоборот, сохраняет правку "move from" и удаляет правку "move to".
self.assertTrue(footnotes[1].is_move_to_revision)
# 4 -  Правка "delete":
# Эта правка возникает, когда мы удаляем текст при отслеживании изменений. Когда мы удаляем текст таким образом,
# он останется в документе как правка, пока мы не примем её,
# что навсегда удалит текст, или отклонит правку, при этом оставив удалённый нами текст на месте.
self.assertTrue(footnotes[3].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [InlineStory](../)

