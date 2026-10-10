---
title: Document.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Document.ensure_minimum method. If the document contains no sections, creates one section with one paragraph."
type: docs
weight: 630
url: /fr/python-net/aspose.words/document/ensure_minimum/
---

## ensure_minimum() {#default}

If the document contains no sections, creates one section with one paragraph.


```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to ensure that a document contains the minimal set of nodes required for editing its contents.

```python
# Un document nouvellement créé contient une Section enfant, qui comprend un Body enfant et un Paragraph enfant.
# Nous pouvons modifier le contenu du Body du document en ajoutant des nœuds tels que Runs ou Shapes en ligne à ce paragraphe.
doc = aw.Document()
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(doc, nodes[0].parent_node)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(nodes[0], nodes[1].parent_node)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
self.assertEqual(nodes[1], nodes[2].parent_node)
# Ceci est l'ensemble minimal de nœuds dont nous avons besoin pour pouvoir modifier le document.
# Nous ne serons plus capables de modifier le document si nous en supprimons l'un d'eux.
doc.remove_all_children()
self.assertEqual(0, len(list(doc.get_child_nodes(aw.NodeType.ANY, True))))
# Appelez cette méthode pour vous assurer que le document possède au moins ces trois nœuds afin que nous puissions le modifier à nouveau.
doc.ensure_minimum()
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
nodes[2].as_paragraph().runs.add(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

