---
title: Inline class
linktitle: Inline class
articleTitle: Inline class
second_title: Aspose.Words for Python
description: "aspose.words.Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own"
type: docs
weight: 670
url: /ar/python-net/aspose.words/inline/
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
# عند تحرير المستند بينما يكون خيار "Track Changes" مفعلًا، الموجود عبر مراجعة -> تتبع،
# يتم تشغيله في Microsoft Word، وتُحسب التغييرات التي نُجريها كمراجعات.
# عند تحرير مستند باستخدام Aspose.Words، يمكننا بدء تتبع المراجعات عن طريق
# استدعاء طريقة "StartTrackRevisions" للمستند وإيقاف التتبع باستخدام طريقة "StopTrackRevisions".
# يمكننا إما قبول المراجعات لدمجها في المستند
# أو رفضها لتغيير التعديل المقترح بفعالية.
self.assertEqual(6, doc.revisions.count)
# العقدة الأصلية للمراجعة هي الـ Run الذي تتعلق به المراجعة. الـ Run هو عقدة Inline.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# فيما يلي خمسة أنواع من المراجعات التي يمكن أن تضع علامة على عقدة Inline.
# 1 -  مراجعة "insert":
# تحدث هذه المراجعة عندما نقوم بإدراج نص أثناء تتبع التغييرات.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  مراجعة "format":
# تحدث هذه المراجعة عندما نغير تنسيق النص أثناء تتبع التغييرات.
self.assertTrue(runs[2].is_format_revision)
# 3 -  مراجعة "move from":
# عندما نحدد نصًا في Microsoft Word، ثم نسحبه إلى مكان مختلف في المستند
# أثناء تتبع التغييرات، تظهر مراجعتان.
# مراجعة "move from" هي نسخة من النص الأصلي قبل أن نقوم بنقله.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  مراجعة "move to":
# مراجعة "move to" هي النص الذي نقلناه إلى موقعه الجديد في المستند.
# مراجعات "Move from" و "move to" تظهر في أزواج لكل عملية نقل نقوم بها.
# قبول مراجعة النقل يحذف مراجعة "move from" والنص الخاص بها،
# ويحتفظ بالنص من مراجعة "move to".
# رفض مراجعة النقل على العكس يحتفظ بمراجعة "move from" ويحذف مراجعة "move to".
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  مراجعة "delete":
# تحدث هذه المراجعة عندما نحذف نصًا أثناء تتبع التغييرات. عندما نحذف النص بهذه الطريقة،
# سيبقى في المستند كمراجعة حتى نقبل المراجعة،
# والتي ستحذف النص نهائيًا، أو ترفض المراجعة، والتي ستحافظ على النص الذي حذفناه في مكانه.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../)
* class [Node](../node/)

