---
title: Inline class
linktitle: Inline class
articleTitle: Inline class
second_title: Aspose.Words for Python
description: "aspose.words.Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own"
type: docs
weight: 670
url: /tr/python-net/aspose.words/inline/
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
# Belgeyi düzenlerken, Review -> Tracking üzerinden bulunan "Track Changes" seçeneği,
# Microsoft Word'de etkinleştirildiğinde, uyguladığımız değişiklikler revizyon olarak sayılır.
# Aspose.Words kullanarak bir belgeyi düzenlerken, revizyon takibini başlatabiliriz
# belgenin "StartTrackRevisions" metodunu çağırarak ve "StopTrackRevisions" metodunu kullanarak takibi durdurabilirsiniz.
# Revizyonları kabul ederek belgeye dahil edebiliriz
# ya da reddederek önerilen değişikliği etkili bir şekilde iptal edebiliriz.
self.assertEqual(6, doc.revisions.count)
# Bir revizyonun üst düğümü, revizyonun ilgili olduğu run'dur. Run, bir Inline düğümdür.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Aşağıda bir Inline düğümünü işaretleyebilen beş revizyon türü bulunmaktadır.
# 1 -  Bir "insert" revizyonu:
# Bu revizyon, değişiklikleri izlerken metin eklediğimizde oluşur.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Bir "format" revizyonu:
# Bu revizyon, değişiklikleri izlerken metnin biçimini değiştirdiğimizde oluşur.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Bir "move from" revizyonu:
# Microsoft Word'de metni vurguladığımızda ve ardından belge içinde farklı bir konuma sürüklediğimizde
# değişiklikleri izlerken iki revizyon ortaya çıkar.
# "move from" revizyonu, metnin taşınmadan önceki bir kopyasıdır.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Bir "move to" revizyonu:
# "move to" revizyonu, belge içinde yeni konumunda taşınan metindir.
# "Move from" ve "move to" revizyonları, gerçekleştirdiğimiz her taşıma revizyonu için çiftler halinde görünür.
# Bir taşıma revizyonunu kabul etmek, "move from" revizyonunu ve metnini siler,
# ve "move to" revizyonundaki metni tutar.
# Bir taşıma revizyonunu reddetmek ise "move from" revizyonunu tutar ve "move to" revizyonunu siler.
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Bir "delete" revizyonu:
# Bu revizyon, değişiklikleri izlerken metin sildiğimizde oluşur. Böyle bir metni sildiğimizde,
# belge içinde bir revizyon olarak kalır, ta ki revizyonu kabul edene kadar,
# metni kalıcı olarak silecek, ya da revizyonu reddedecek; bu, sildiğimiz metni olduğu yerde tutacak.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../)
* class [Node](../node/)

