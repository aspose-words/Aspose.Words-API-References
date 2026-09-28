---
title: Document.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Document.ensure_minimum method. If the document contains no sections, creates one section with one paragraph."
type: docs
weight: 630
url: /zh/python-net/aspose.words/document/ensure_minimum/
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
# 新创建的文档包含一个子节（Section），其中包括一个子主体（Body）和一个子段落（Paragraph）。
# 我们可以通过向该段落添加诸如 Run 或内联 Shape 等节点来编辑文档主体的内容。
doc = aw.Document()
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(doc, nodes[0].parent_node)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(nodes[0], nodes[1].parent_node)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
self.assertEqual(nodes[1], nodes[2].parent_node)
# 这是我们编辑文档所需的最小节点集。
# 如果我们移除其中任何一个节点，将无法再编辑文档。
doc.remove_all_children()
self.assertEqual(0, len(list(doc.get_child_nodes(aw.NodeType.ANY, True))))
# 调用此方法以确保文档至少拥有这三个节点，从而可以再次编辑它。
doc.ensure_minimum()
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
nodes[2].as_paragraph().runs.add(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

