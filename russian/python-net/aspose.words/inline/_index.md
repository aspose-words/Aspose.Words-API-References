---
title: Inline class
linktitle: Inline class
articleTitle: Inline class
second_title: Aspose.Words for Python
description: "aspose.words.Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own"
type: docs
weight: 670
url: /ru/python-net/aspose.words/inline/
---

## Inline class

Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own.
To learn more, visit the [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/python-net/logical-levels-of-nodes-in-a-document/) documentation article.




### Remarks

A class derived from [Inline](./) can be a child of [Paragraph](../paragraph/).




**Inheritance:** [Inline](./) → [Node](../node/)

### Properties

| Name | Description |
| --- | --- |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [font](./font/) | Provides access to the font formatting of this object. |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [is_delete_revision](./is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [is_format_revision](./is_format_revision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [is_insert_revision](./is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [is_move_from_revision](./is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [is_move_to_revision](./is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_type](../node/node_type/) | Gets the type of this node.<br>(Inherited from [Node](../node/)) |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parent_paragraph](./parent_paragraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node. |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../node/)) |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_text()](../node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

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

* module [aspose.words](../)
* class [Node](../node/)

