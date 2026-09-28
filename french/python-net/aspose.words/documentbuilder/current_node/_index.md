---
title: DocumentBuilder.current_node property
linktitle: current_node property
articleTitle: current_node property
second_title: Aspose.Words for Python
description: "DocumentBuilder.current_node property. Gets the node that is currently selected in this DocumentBuilder."
type: docs
weight: 40
url: /fr/python-net/aspose.words/documentbuilder/current_node/
---

## DocumentBuilder.current_node property

Gets the node that is currently selected in this DocumentBuilder.


```python
@property
def current_node(self) -> aspose.words.Node:
    ...

```

### Remarks

[DocumentBuilder.current_node](./) is a cursor of [DocumentBuilder](../) and points to a [Node](../../node/)
that is a direct child of a [Paragraph](../../paragraph/). Any insert operations you perform using
[DocumentBuilder](../) will insert before the [DocumentBuilder.current_node](./).

When the current paragraph is empty or the cursor is positioned just
before the end of a paragraph or structured document tag, [DocumentBuilder.current_node](./) returns ``None``.




### Examples

Shows how to move a document builder's cursor to different nodes in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Créer un signet valide, une entité qui consiste en des nœuds entourés par un nœud de début de signet,
# et un nœud de fin de signet.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# Le curseur du constructeur de document est toujours en avance sur le nœud que nous avons ajouté en dernier avec lui.
# Si le curseur du constructeur se trouve à la fin du document, son nœud actuel sera nul.
# Le nœud précédent est le nœud de fin de signet que nous avons ajouté en dernier.
# Ajouter de nouveaux nœuds avec le constructeur les ajoutera à la suite du dernier nœud.
self.assertIsNone(builder.current_node)
# Si nous souhaitons modifier une autre partie du document avec le constructeur,
# nous devrons amener son curseur au nœud que nous souhaitons modifier.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# Le déplacer vers un signet le déplacera vers le premier nœud compris entre les nœuds de début et de fin du signet, le texte encapsulé.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# Nous pouvons également déplacer le curseur vers un nœud individuel de cette façon.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# Nous pouvons utiliser des méthodes spécifiques pour nous déplacer au début ou à la fin d'un document.
builder.move_to_document_end()
self.assertTrue(builder.is_at_end_of_paragraph)
builder.move_to_document_start()
self.assertTrue(builder.is_at_start_of_paragraph)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)
* property [DocumentBuilder.current_paragraph](../current_paragraph/)
* property [DocumentBuilder.current_structured_document_tag](../current_structured_document_tag/)

