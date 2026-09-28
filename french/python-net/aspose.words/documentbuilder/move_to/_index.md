---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /fr/python-net/aspose.words/documentbuilder/move_to/
---

## move_to(node) {#node}

Moves the cursor to an inline node or to the end of a paragraph.


```python
def move_to(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node must be a paragraph or a direct child of a paragraph. |

### Remarks

When *node* is an inline-level node, the cursor is moved to this node
and further content will be inserted before that node.

When *node* is a [Paragraph](../../paragraph/), the cursor is moved to the end of the paragraph
and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node
and further content will be inserted just before the paragraph break.




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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# Le constructeur de document possède un curseur, qui agit comme la partie du document
# où le constructeur ajoute de nouveaux nœuds lorsque nous utilisons ses méthodes de construction de document.
# Ce curseur fonctionne de la même manière que le curseur clignotant de Microsoft Word,
# et il se retrouve toujours immédiatement après tout nœud que le constructeur vient d'insérer.
# Pour ajouter du contenu à une autre partie du document,
# nous pouvons déplacer le curseur vers un nœud différent avec la méthode "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Le curseur est maintenant devant le nœud vers lequel nous l'avons déplacé.
# Ajouter un deuxième segment l'insérera devant le premier segment.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Déplacez le curseur à la fin du document pour continuer à ajouter du texte à la fin comme auparavant.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

