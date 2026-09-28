---
title: Inline class
linktitle: Inline class
articleTitle: Inline class
second_title: Aspose.Words for Python
description: "aspose.words.Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own"
type: docs
weight: 670
url: /zh/python-net/aspose.words/inline/
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
# 当我们在文档中编辑时，开启位于 Review -> Tracking 中的 "Track Changes" 选项，
# 在 Microsoft Word 中打开后，我们所做的更改会计为修订。
# 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订：
# 调用文档的 "StartTrackRevisions" 方法开始跟踪，使用 "StopTrackRevisions" 方法停止跟踪。
# 我们可以接受修订，将其合并到文档中
# 或拒绝它们，以有效撤销所提议的更改。
self.assertEqual(6, doc.revisions.count)
# 修订的父节点是该修订涉及的 Run。Run 是一种 Inline 节点。
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# 下面列出了可以标记 Inline 节点的五种修订类型。
# 1 -  一个 "insert" 修订：
# 当我们在跟踪更改时插入文本时，会产生此修订。
self.assertTrue(runs[2].is_insert_revision)
# 2 -  一个 "format" 修订：
# 当我们在跟踪更改时更改文本的格式时，会产生此修订。
self.assertTrue(runs[2].is_format_revision)
# 3 -  一个 "move from" 修订：
# 当我们在 Microsoft Word 中突出显示文本，然后将其拖动到文档的其他位置时
# 在跟踪更改的情况下，会出现两个修订。
# "move from" 修订是我们移动之前原始文本的副本。
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  一个 "move to" 修订：
# "move to" 修订是我们在文档中新位置的移动文本。
# "Move from" 和 "move to" 修订会成对出现，针对我们执行的每一次移动修订。
# 接受移动修订会删除 "move from" 修订及其文本，
# 并保留 "move to" 修订中的文本。
# 相反，拒绝移动修订会保留 "move from" 修订并删除 "move to" 修订。
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  一个 "delete" 修订：
# 当我们在跟踪更改时删除文本时，会产生此修订。当我们这样删除文本时，
# 它会作为修订保留在文档中，直到我们接受该修订，
# 这将永久删除文本，或拒绝修订，后者会保留我们已删除的文本在原位置。
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../)
* class [Node](../node/)

