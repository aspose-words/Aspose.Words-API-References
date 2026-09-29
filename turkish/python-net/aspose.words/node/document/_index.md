---
title: Node.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "Node.document property. Gets the document to which this node belongs."
type: docs
weight: 20
url: /tr/python-net/aspose.words/node/document/
---

## Node.document property

Gets the document to which this node belongs.


```python
@property
def document(self) -> aspose.words.DocumentBase:
    ...

```

### Remarks

The node always belongs to a document even if it has just been created
and not yet added to the tree, or if it has been removed from the tree.




### Examples

Shows how to create a node and set its owning document.

```python
from api_example_base import ApiExampleBase
doc = aw.Document()
para = aw.Paragraph(doc)
para.append_child(aw.Run(doc=doc, text='Hello world!'))
# Bu paragrafı henüz herhangi bir birleşik düğüme çocuk olarak eklemedik.
self.assertIsNone(para.parent_node)
# Bir düğüm, başka bir birleşik düğümün uygun bir çocuk düğüm türüyse,
# her iki düğümün aynı sahip belgeye sahip olması durumunda sadece çocuk olarak ekleyebiliriz.
# Sahip belge, düğümün yapıcı metoduna gönderdiğimiz belgedir.
# Bu paragrafı belgeye eklemedik, bu yüzden belge onun metnini içermiyor.
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# Belge bu paragrafın sahibi olduğundan, paragrafın içeriğine stillerinden birini uygulayabiliriz.
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# Bu düğümü belgeye ekleyin ve ardından içeriğini doğrulayın.
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

