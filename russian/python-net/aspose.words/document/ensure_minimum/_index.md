---
title: Document.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Document.ensure_minimum method. If the document contains no sections, creates one section with one paragraph."
type: docs
weight: 630
url: /ru/python-net/aspose.words/document/ensure_minimum/
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
# Новый созданный документ содержит один дочерний Section, который включает один дочерний Body и один дочерний Paragraph.
# Мы можем редактировать содержимое тела документа, добавляя узлы, такие как Runs или встроенные Shapes, в этот абзац.
doc = aw.Document()
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(doc, nodes[0].parent_node)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(nodes[0], nodes[1].parent_node)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
self.assertEqual(nodes[1], nodes[2].parent_node)
# Это минимальный набор узлов, необходимых для редактирования документа.
# Мы больше не сможем редактировать документ, если удалим любой из них.
doc.remove_all_children()
self.assertEqual(0, len(list(doc.get_child_nodes(aw.NodeType.ANY, True))))
# Вызовите этот метод, чтобы убедиться, что документ имеет как минимум эти три узла, чтобы мы могли снова его редактировать.
doc.ensure_minimum()
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
nodes[2].as_paragraph().runs.add(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

