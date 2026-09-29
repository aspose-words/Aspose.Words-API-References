---
title: Paragraph.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "Paragraph.node_type property. Returns [NodeType.PARAGRAPH](../../nodetype/#PARAGRAPH)."
type: docs
weight: 170
url: /sv/python-net/aspose.words/paragraph/node_type/
---

## Paragraph.node_type property

Returns [NodeType.PARAGRAPH](../../nodetype/#PARAGRAPH).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to traverse a composite node's tree of child nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Alla noder som kan innehålla undernoder, såsom själva dokumentet, är sammansatta.
self.assertTrue(doc.is_composite)
# Anropa den rekursiva funktionen som går igenom och skriver ut alla undernoder i en sammansatt nod.
self.traverse_all_nodes(doc, 0)
```

Shows how to traverse a composite node's tree of child nodes (TraverseAllNodes).

```python
def traverse_all_nodes(self, parent_node, depth):
    child_node = parent_node.first_child
    while child_node != None:
        sys.stdout.write(f'\t' * depth + aw.Node.node_type_to_string(child_node.node_type))
        # Rekursion in i noden om den är en sammansatt nod. Annars skrivs dess innehåll ut om den är en inline-nod.
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
* class [Paragraph](../)

