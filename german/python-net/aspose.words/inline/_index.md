---
title: Inline class
linktitle: Inline class
articleTitle: Inline class
second_title: Aspose.Words for Python
description: "aspose.words.Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own"
type: docs
weight: 670
url: /de/python-net/aspose.words/inline/
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
# Wenn wir das Dokument bearbeiten, während die Option "Track Changes", zu finden über Review -> Tracking,
# in Microsoft Word aktiviert ist, zählen die von uns vorgenommenen Änderungen als Revisionen.
# Beim Bearbeiten eines Dokuments mit Aspose.Words können wir die Verfolgung von Revisionen beginnen, indem wir
# die Methode "StartTrackRevisions" des Dokuments aufrufen und die Verfolgung mit der Methode "StopTrackRevisions" beenden.
# Wir können Revisionen entweder akzeptieren, um sie in das Dokument zu übernehmen
# oder sie ablehnen, um die vorgeschlagene Änderung wirksam zu entfernen.
self.assertEqual(6, doc.revisions.count)
# Der übergeordnete Knoten einer Revision ist der Run, auf den sich die Revision bezieht. Ein Run ist ein Inline‑Knoten.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Unten sind fünf Arten von Revisionen aufgeführt, die einen Inline‑Knoten kennzeichnen können.
# 1 -  Eine "insert"‑Revision:
# Diese Revision tritt auf, wenn wir Text einfügen, während Änderungen verfolgt werden.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Eine "format"‑Revision:
# Diese Revision tritt auf, wenn wir die Formatierung von Text ändern, während Änderungen verfolgt werden.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Eine "move from"‑Revision:
# Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
# während Änderungen verfolgt werden, erscheinen zwei Revisionen.
# Die "move from"‑Revision ist eine Kopie des Textes, wie er ursprünglich vor dem Verschieben war.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Eine "move to"‑Revision:
# Die "move to"‑Revision ist der Text, den wir an seiner neuen Position im Dokument verschoben haben.
# "Move from"‑ und "move to"‑Revisionen erscheinen paarweise für jede durchgeführte Verschieberevision.
# Das Akzeptieren einer Verschieberevision löscht die "move from"‑Revision und deren Text,
# und behält den Text der "move to"‑Revision bei.
# Das Ablehnen einer Verschieberevision hingegen behält die "move from"‑Revision und löscht die "move to"‑Revision.
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Eine "delete"‑Revision:
# Diese Revision tritt auf, wenn wir Text löschen, während Änderungen verfolgt werden. Wenn wir Text auf diese Weise löschen,
# bleibt er im Dokument als Revision, bis wir die Revision entweder akzeptieren,
# die den Text dauerhaft löscht, oder die Revision ablehnt, die den gelöschten Text an seiner Stelle belässt.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../)
* class [Node](../node/)

