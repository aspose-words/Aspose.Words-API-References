---
title: RunCollection indexer
linktitle: RunCollection indexer
articleTitle: RunCollection indexer
second_title: Aspose.Words for Python
description: "RunCollection indexer. Retrieves a [Run](../../run/) at the given index."
type: docs
weight: 10
url: /ru/python-net/aspose.words/runcollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [Run](../../run/) at the given index.



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

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# Когда мы редактируем документ при включённой опции "Track Changes", доступной через Review -> Tracking,
# включена в Microsoft Word, изменения, которые мы вносим, считаются правками.
# При редактировании документа с использованием Aspose.Words мы можем начать отслеживание правок, вызвав
# вызов метода документа "StartTrackRevisions" и прекратить отслеживание, используя метод "StopTrackRevisions".
# Мы можем либо принять правки, чтобы интегрировать их в документ
# либо отклонить их, чтобы эффективно отменить предложенное изменение.
self.assertEqual(6, doc.revisions.count)
# Родительским узлом правки является run, к которому относится правка. Run — это Inline‑узел.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Ниже перечислены пять типов правок, которые могут пометить Inline‑узел.
# 1 -  Правка "insert":
# Эта правка возникает, когда мы вставляем текст при отслеживании изменений.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Правка "format":
# Эта правка возникает, когда мы изменяем форматирование текста при отслеживании изменений.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Правка "move from":
# Когда мы выделяем текст в Microsoft Word и затем перетаскиваем его в другое место в документе
# при отслеживании изменений появляются две правки.
# Правка "move from" представляет собой копию исходного текста до его перемещения.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Правка "move to":
# Правка "move to" — это текст, который мы переместили в его новое положение в документе.
# "Move from" и "move to" правки появляются парами для каждого перемещения, которое мы выполняем.
# Принятие перемещения удаляет правку "move from" и её текст,
# и сохраняет текст из правки "move to".
# Отклонение перемещения, наоборот, сохраняет правку "move from" и удаляет правку "move to".
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Правка "delete":
# Эта правка возникает, когда мы удаляем текст при отслеживании изменений. Когда мы удаляем текст таким образом,
# он останется в документе как правка, пока мы не примем её,
# что навсегда удалит текст, или отклонит правку, при этом оставив удалённый нами текст на месте.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [RunCollection](../)

