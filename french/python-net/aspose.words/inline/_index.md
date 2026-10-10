---
title: Inline class
linktitle: Inline class
articleTitle: Inline class
second_title: Aspose.Words for Python
description: "aspose.words.Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own"
type: docs
weight: 670
url: /fr/python-net/aspose.words/inline/
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
# Lorsque nous modifions le document alors que l'option "Track Changes", trouvée via Révision -> Suivi,
# est activée dans Microsoft Word, les modifications que nous appliquons sont comptées comme des révisions.
# Lors de la modification d'un document avec Aspose.Words, nous pouvons commencer à suivre les révisions en
# appelant la méthode "StartTrackRevisions" du document et en arrêtant le suivi en utilisant la méthode "StopTrackRevisions".
# Nous pouvons soit accepter les révisions pour les intégrer au document
# ou les rejeter afin de modifier efficacement le changement proposé.
self.assertEqual(6, doc.revisions.count)
# Le nœud parent d'une révision est le run auquel la révision se rapporte. Un Run est un nœud Inline.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Voici cinq types de révisions pouvant marquer un nœud Inline.
# 1 -  Une révision "insert" :
# Cette révision se produit lorsque nous insérons du texte tout en suivant les modifications.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  Une révision "format" :
# Cette révision se produit lorsque nous modifions le formatage du texte tout en suivant les modifications.
self.assertTrue(runs[2].is_format_revision)
# 3 -  Une révision "move from" :
# Lorsque nous sélectionnons du texte dans Microsoft Word, puis le faisons glisser vers un autre emplacement du document
# tout en suivant les modifications, deux révisions apparaissent.
# La révision "move from" est une copie du texte original avant que nous le déplacions.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  Une révision "move to" :
# La révision "move to" est le texte que nous avons déplacé à sa nouvelle position dans le document.
# Les révisions "move from" et "move to" apparaissent par paires pour chaque révision de déplacement que nous effectuons.
# Accepter une révision de déplacement supprime la révision "move from" ainsi que son texte,
# et conserve le texte de la révision "move to".
# Rejeter une révision de déplacement conserve au contraire la révision "move from" et supprime la révision "move to".
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  Une révision "delete" :
# Cette révision se produit lorsque nous supprimons du texte tout en suivant les modifications. Lorsque nous supprimons du texte de cette façon,
# il restera dans le document en tant que révision jusqu'à ce que nous l'acceptions ou le rejetions.
# qui supprimera le texte définitivement, ou rejettera la révision, ce qui gardera le texte que nous avons supprimé à son emplacement.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../)
* class [Node](../node/)

