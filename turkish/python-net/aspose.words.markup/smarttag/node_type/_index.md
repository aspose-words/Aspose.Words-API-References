---
title: SmartTag.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "SmartTag.node_type property. Returns [NodeType.SMART_TAG](../../../aspose.words/nodetype/#SMART_TAG)."
type: docs
weight: 30
url: /tr/python-net/aspose.words.markup/smarttag/node_type/
---

## SmartTag.node_type property

Returns [NodeType.SMART_TAG](../../../aspose.words/nodetype/#SMART_TAG).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to traverse a composite node's tree of child nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Belge gibi kendisi de çocuk düğümler içerebilen herhangi bir düğüm, birleşik bir düğümdür.
self.assertTrue(doc.is_composite)
# Bir birleşik düğümün tüm çocuk düğümlerini dolaşacak ve yazdıracak özyinelemeli fonksiyonu çağırın.
self.traverse_all_nodes(doc, 0)
```

Shows how to traverse a composite node's tree of child nodes (TraverseAllNodes).

```python
def traverse_all_nodes(self, parent_node, depth):
    child_node = parent_node.first_child
    while child_node != None:
        sys.stdout.write(f'\t' * depth + aw.Node.node_type_to_string(child_node.node_type))
        # Düğüm bir birleşik düğümse içine özyinelemeli olarak girin. Aksi takdirde, eğer satır içi bir düğümse içeriğini yazdırın.
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

* module [aspose.words.markup](../../)
* class [SmartTag](../)

