---
title: ParagraphCollection class
linktitle: ParagraphCollection class
articleTitle: ParagraphCollection class
second_title: Aspose.Words for Python
description: "aspose.words.ParagraphCollection class. Provides typed access to a collection of [Paragraph](../paragraph/) nodes"
type: docs
weight: 980
url: /de/python-net/aspose.words/paragraphcollection/
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
# Dieses Dokument enthält "Move"‑Revisionen, die erscheinen, wenn wir Text mit dem Cursor markieren,
# und ihn dann ziehen, um ihn an einen anderen Ort zu verschieben
# während Revisionen in Microsoft Word über "Review" → "Track changes" nachverfolgt werden.
self.assertEqual(6, len(list(filter(lambda r: r.revision_type == aw.RevisionType.MOVING, doc.revisions))))
paragraphs = doc.first_section.body.paragraphs
# Move‑Revisionen bestehen aus Paaren von "Move from"‑ und "Move to"‑Revisionen.
# Diese Revisionen sind potenzielle Änderungen am Dokument, die wir entweder akzeptieren oder ablehnen können.
# Bevor wir eine Move‑Revision akzeptieren/ablehnen, muss das Dokument
# muss sowohl den Abgangs- als auch den Ankunftsort des Textes nachverfolgen.
# Der zweite und der vierte Absatz definieren eine solche Revision und haben daher denselben Inhalt.
self.assertEqual(paragraphs[1].get_text(), paragraphs[3].get_text())
# Die "Move from"‑Revision ist der Absatz, von dem wir den Text gezogen haben.
# Wenn wir die Revision akzeptieren, wird dieser Absatz verschwinden,
# und der andere bleibt erhalten und ist nicht mehr eine Revision.
self.assertTrue(paragraphs[1].is_move_from_revision)
# Die "Move to"‑Revision ist der Absatz, zu dem wir den Text gezogen haben.
# Wenn wir die Revision ablehnen, wird stattdessen dieser Absatz verschwinden, und der andere bleibt erhalten.
self.assertTrue(paragraphs[3].is_move_to_revision)
```

### See Also

* module [aspose.words](../)
* class [NodeCollection](../nodecollection/)

