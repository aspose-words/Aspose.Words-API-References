---
title: ParagraphCollection class
linktitle: ParagraphCollection class
articleTitle: ParagraphCollection class
second_title: Aspose.Words for Python
description: "aspose.words.ParagraphCollection class. Provides typed access to a collection of [Paragraph](../paragraph/) nodes"
type: docs
weight: 980
url: /ru/python-net/aspose.words/paragraphcollection/
---

## ParagraphCollection class

Provides typed access to a collection of [Paragraph](../paragraph/) nodes.
To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/python-net/working-with-paragraphs/) documentation article.




**Inheritance:** [ParagraphCollection](./) → [NodeCollection](../nodecollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Retrieves a [Paragraph](../paragraph/) at the given index. |

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
|[ to_array()](./to_array/#default) | Copies all paragraphs from the collection to a new array of paragraphs. |

### Examples

Shows how to check whether a paragraph is a move revision.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Этот документ содержит правки "Move", которые появляются, когда мы выделяем текст курсором,
# а затем перетаскиваем его, чтобы переместить в другое место
# при отслеживании правок в Microsoft Word через "Review" -> "Track changes".
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Правки перемещения состоят из пар правок "Move from" и "Move to".
# Эти правки являются потенциальными изменениями документа, которые мы можем либо принять, либо отклонить.
# Прежде чем мы примем/отклоним правку перемещения, документ
# должен отслеживать как исходные, так и конечные места текста.
# Второй и четвертый абзацы определяют одну такую правку, поэтому оба имеют одинаковое содержание.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# Правка "Move from" — это абзац, из которого мы перетаскивали текст.
# Если мы примем правку, этот абзац исчезнет,
# а другой останется и больше не будет правкой.
self.assertTrue(paragraphs[1].is_move_from_revision)
# Правка "Move to" — это абзац, в который мы перетаскивали текст.
# Если мы отклоним правку, вместо этого исчезнет этот абзац, а другой останется.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

