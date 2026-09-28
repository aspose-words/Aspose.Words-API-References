---
title: Document.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Document.ensure_minimum method. If the document contains no sections, creates one section with one paragraph."
type: docs
weight: 630
url: /ar/python-net/aspose.words/document/ensure_minimum/
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
# المستند الذي تم إنشاؤه حديثًا يحتوي على قسم فرعي واحد، والذي يتضمن جسمًا فرعيًا واحدًا وفقرة فرعية واحدة.
# يمكننا تعديل محتويات جسم المستند بإضافة عقد مثل Runs أو Shapes داخلية إلى تلك الفقرة.
doc = aw.Document()
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(doc, nodes[0].parent_node)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(nodes[0], nodes[1].parent_node)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
self.assertEqual(nodes[1], nodes[2].parent_node)
# هذه هي مجموعة العقد الدنيا التي نحتاجها لنتمكن من تعديل المستند.
# لن نتمكن بعد ذلك من تعديل المستند إذا قمنا بإزالة أي منها.
doc.remove_all_children()
self.assertEqual(0, len(list(doc.get_child_nodes(aw.NodeType.ANY, True))))
# استدعِ هذه الطريقة للتأكد من أن المستند يحتوي على تلك العقد الثلاث على الأقل حتى نتمكن من تعديلها مرة أخرى.
doc.ensure_minimum()
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
nodes[2].as_paragraph().runs.add(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

