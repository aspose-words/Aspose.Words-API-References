---
title: Document.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Document.ensure_minimum method. If the document contains no sections, creates one section with one paragraph."
type: docs
weight: 630
url: /sv/python-net/aspose.words/document/ensure_minimum/
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
# Ett nyss skapat dokument innehåller en undersektion Section, som inkluderar en undersektion Body och en undersektion Paragraph.
# Vi kan redigera dokumentets Body-innehåll genom att lägga till noder såsom Runs eller inline Shapes till det stycket.
doc = aw.Document()
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(doc, nodes[0].parent_node)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(nodes[0], nodes[1].parent_node)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
self.assertEqual(nodes[1], nodes[2].parent_node)
# Detta är den minsta uppsättningen av noder som vi behöver för att kunna redigera dokumentet.
# Vi kommer inte längre kunna redigera dokumentet om vi tar bort någon av dem.
doc.remove_all_children()
self.assertEqual(0, len(list(doc.get_child_nodes(aw.NodeType.ANY, True))))
# Anropa den här metoden för att säkerställa att dokumentet har minst dessa tre noder så att vi kan redigera det igen.
doc.ensure_minimum()
self.assertEqual(aw.NodeType.SECTION, nodes[0].node_type)
self.assertEqual(aw.NodeType.BODY, nodes[1].node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, nodes[2].node_type)
nodes[2].as_paragraph().runs.add(aw.Run(doc=doc, text='Hello world!'))
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

