---
title: Node.parent_node property
linktitle: parent_node property
articleTitle: parent_node property
second_title: Aspose.Words for Python
description: "Node.parent_node property. Gets the immediate parent of this node."
type: docs
weight: 60
url: /sv/python-net/aspose.words/node/parent_node/
---

## Node.parent_node property

Gets the immediate parent of this node.


```python
@property
def parent_node(self) -> aspose.words.CompositeNode:
    ...

```

### Remarks

If a node has just been created and not yet added to the tree,
or if it has been removed from the tree, the parent is ``None``.




### Examples

Shows how to create a node and set its owning document.

```python
from api_example_base import ApiExampleBase
doc = aw.Document()
para = aw.Paragraph(doc)
para.append_child(aw.Run(doc=doc, text='Hello world!'))
# Vi har ännu inte lagt till detta stycke som ett barn till någon sammansatt nod.
self.assertIsNone(para.parent_node)
# Om en nod är en lämplig barnnodtyp för en annan sammansatt nod,
# kan vi fästa den som ett barn endast om båda noderna har samma ägardokument.
# Ägardokumentet är det dokument vi skickade till nodens konstruktor.
# Vi har inte bifogat detta stycke till dokumentet, så dokumentet innehåller inte dess text.
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# Eftersom dokumentet äger detta stycke kan vi applicera en av dess stilar på styckets innehåll.
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# Lägg till denna nod i dokumentet och verifiera sedan dess innehåll.
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

