---
title: FieldEnd.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "FieldEnd.node_type property. Returns [NodeType.FIELD_END](../../../aspose.words/nodetype/#FIELD_END)."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldend/node_type/
---

## FieldEnd.node_type property

Returns [NodeType.FIELD_END](../../../aspose.words/nodetype/#FIELD_END).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to traverse a composite node's tree of child nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# 任何可以包含子节点的节点，例如文档本身，都是复合节点。
self.assertTrue(doc.is_composite)
# 调用递归函数，遍历并打印复合节点的所有子节点。
self.traverse_all_nodes(doc, 0)
```

Shows how to traverse a composite node's tree of child nodes (TraverseAllNodes).

```python
def traverse_all_nodes(self, parent_node, depth):
    child_node = parent_node.first_child
    while child_node != None:
        sys.stdout.write(f'\t' * depth + aw.Node.node_type_to_string(child_node.node_type))
        # 如果节点是复合节点则递归进入；否则，如果是内联节点则打印其内容。
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

* module [aspose.words.fields](../../)
* class [FieldEnd](../)

