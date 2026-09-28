---
title: Run.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "Run.node_type property. Returns [NodeType.RUN](../../nodetype/#RUN)."
type: docs
weight: 30
url: /fr/python-net/aspose.words/run/node_type/
---

## Run.node_type property

Returns [NodeType.RUN](../../nodetype/#RUN).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to traverse a composite node's tree of child nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Tout nœud pouvant contenir des nœuds enfants, comme le document lui‑-même, est composite.
self.assertTrue(doc.is_composite)
# Appelez la fonction récursive qui parcourra et affichera tous les nœuds enfants d'un nœud composite.
self.traverse_all_nodes(doc, 0)
```

Shows how to traverse a composite node's tree of child nodes (TraverseAllNodes).

```python
def traverse_all_nodes(self, parent_node, depth):
    child_node = parent_node.first_child
    while child_node != None:
        sys.stdout.write(f'\t' * depth + aw.Node.node_type_to_string(child_node.node_type))
        # Récursivement parcourir le nœud s'il s'agit d'un nœud composite. Sinon, afficher son contenu s'il s'agit d'un nœud en ligne.
        if child_node.is_composite:
            sys.stdout.write('\n')
            self.traverse_all_nodes(child_node.as_composite_node(), depth + 1)
        elif isinstance(child_node, aw.Inline):
            sys.stdout.write(f' - "{child_node.get_text().strip()}"\n')
        else:
            sys.stdout.write('\n')
        child_node = child_node.next_sibling
```

### See Also

* module [aspose.words](../../)
* class [Run](../)

