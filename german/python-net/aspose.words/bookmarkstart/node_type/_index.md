---
title: BookmarkStart.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "BookmarkStart.node_type property. Returns [NodeType.BOOKMARK_START](../../nodetype/#BOOKMARK_START)."
type: docs
weight: 40
url: /de/python-net/aspose.words/bookmarkstart/node_type/
---

## BookmarkStart.node_type property

Returns [NodeType.BOOKMARK_START](../../nodetype/#BOOKMARK_START).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to traverse a composite node's tree of child nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Jeder Knoten, der Kindknoten enthalten kann, wie das Dokument selbst, ist zusammengesetzt.
self.assertTrue(doc.is_composite)
# Rufen Sie die rekursive Funktion auf, die alle Kindknoten eines zusammengesetzten Knotens durchläuft und ausgibt.
self.traverse_all_nodes(doc, 0)
```

Shows how to traverse a composite node's tree of child nodes (TraverseAllNodes).

```python
def traverse_all_nodes(self, parent_node, depth):
    child_node = parent_node.first_child
    while child_node != None:
        sys.stdout.write(f'\t' * depth + aw.Node.node_type_to_string(child_node.node_type))
        # Rekursieren Sie in den Knoten, wenn er ein zusammengesetzter Knoten ist. Andernfalls geben Sie seinen Inhalt aus, wenn er ein Inline‑Knoten ist.
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
* class [BookmarkStart](../)

