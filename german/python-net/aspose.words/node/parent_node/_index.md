---
title: Node.parent_node property
linktitle: parent_node property
articleTitle: parent_node property
second_title: Aspose.Words for Python
description: "Node.parent_node property. Gets the immediate parent of this node."
type: docs
weight: 60
url: /de/python-net/aspose.words/node/parent_node/
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
# Wir haben diesen Absatz noch nicht als Kind zu einem zusammengesetzten Knoten hinzugefügt.
self.assertIsNone(para.parent_node)
# Wenn ein Knoten ein geeigneter Kindknotentyp eines anderen zusammengesetzten Knotens ist,
# können wir ihn nur als Kind anhängen, wenn beide Knoten dasselbe Eigentümerdokument haben.
# Das Eigentümerdokument ist das Dokument, das wir dem Konstruktor des Knotens übergeben haben.
# Wir haben diesen Absatz nicht an das Dokument angehängt, sodass das Dokument dessen Text nicht enthält.
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# Da das Dokument diesen Absatz besitzt, können wir einen seiner Stile auf den Inhalt des Absatzes anwenden.
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# Fügen Sie diesen Knoten dem Dokument hinzu und überprüfen Sie anschließend dessen Inhalt.
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

