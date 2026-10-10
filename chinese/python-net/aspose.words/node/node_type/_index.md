---
title: Node.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "Node.node_type property. Gets the type of this node."
type: docs
weight: 50
url: /zh/python-net/aspose.words/node/node_type/
---

## Node.node_type property

Gets the type of this node.


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

Shows how to remove all child nodes of a specific type from a composite node.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
self.assertEqual(2, doc.get_child_nodes(aw.NodeType.TABLE, True).count)
cur_node = doc.first_section.body.first_child
while cur_node != None:
    # 将下一个兄弟节点保存为变量，以防我们在删除此节点后想要移动到它。
    next_node = cur_node.next_sibling
    # 节主体可以包含 Paragraph 和 Table 节点。
    # 如果节点是 Table，则将其从父节点中移除。
    if cur_node.node_type == aw.NodeType.TABLE:
        cur_node.remove()
    cur_node = next_node
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.TABLE, True).count)
```

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
node = doc.first_section.body.first_child
while node != None:
    print()
    print(f'Node type: {aw.Node.node_type_to_string(node.node_type)}')
    contents = node.get_text().strip()
    print('This node contains no text' if contents == '' else f'Contents: "{node.get_text().strip()}"')
    node = node.next_sibling
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

