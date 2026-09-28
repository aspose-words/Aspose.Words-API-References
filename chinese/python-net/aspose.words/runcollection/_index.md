---
title: RunCollection class
linktitle: RunCollection class
articleTitle: RunCollection class
second_title: Aspose.Words for Python
description: "aspose.words.RunCollection class. Provides typed access to a collection of [Run](../run/) nodes"
type: docs
weight: 1120
url: /zh/python-net/aspose.words/runcollection/
---

## RunCollection class

Provides typed access to a collection of [Run](../run/) nodes.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




**Inheritance:** [RunCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Run](../run/) at the given index. |

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ index_of(node)](../nodecollection/index_of/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#int_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ remove_at(index)](../nodecollection/remove_at/#int) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ to_array()](./to_array/#default) | Copies all runs from the collection to a new array of runs. |

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
* class [NodeCollection](../nodecollection/)

