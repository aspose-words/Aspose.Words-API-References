---
title: FieldSeparator.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "FieldSeparator.node_type property. Returns [NodeType.FIELD_SEPARATOR](../../../aspose.words/nodetype/#FIELD_SEPARATOR)."
type: docs
weight: 10
url: /python-net/aspose.words.fields/fieldseparator/node_type/
---

## FieldSeparator.node_type property

Returns [NodeType.FIELD_SEPARATOR](../../../aspose.words/nodetype/#FIELD_SEPARATOR).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to traverse a composite node's tree of child nodes.

```python
def test_recurse_children(self):

    doc = aw.Document(MY_DIR + "Paragraphs.docx")

    # Any node that can contain child nodes, such as the document itself, is composite.
    self.assertTrue(doc.is_composite)

    # Invoke the recursive function that will go through and print all the child nodes of a composite node.
    ExNode.traverse_all_nodes(doc, 0)

@staticmethod
def traverse_all_nodes(parent_node: aw.CompositeNode, depth: int):
    """Recursively traverses a node tree while printing the type of each node
    with an indent depending on depth as well as the contents of all inline nodes."""

    child_node = parent_node.first_child
    while child_node is not None:

        print("\t" * depth + aw.Node.node_type_to_string(child_node.node_type), end="")

        # Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
        if child_node.is_composite:
            print()
            ExNode.traverse_all_nodes(child_node.as_composite_node(), depth + 1)

        elif child_node is aw.Inline:
            print(f" - \"{child_node.get_text().strip()}\"")

        else:
            print()

        child_node = child_node.next_sibling
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeparator](../)

