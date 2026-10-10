---
title: Node.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "Node.document property. Gets the document to which this node belongs."
type: docs
weight: 20
url: /ar/python-net/aspose.words/node/document/
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
# لم نقم بعد بإلحاق هذه الفقرة كطفل لأي عقدة مركبة.
self.assertIsNone(para.parent_node)
# إذا كانت العقدة نوعًا مناسبًا من العقد الفرعية لعقدة مركبة أخرى،
# يمكننا إرفاقها كطفل فقط إذا كان كلا العقدتين لهما نفس مستند المالك.
# مستند المالك هو المستند الذي مررناه إلى مُنشئ العقدة.
# لم نقم بإرفاق هذه الفقرة إلى المستند، لذا لا يحتوي المستند على نصها.
self.assertEqual(para.document, doc)
self.assertEqual('', doc.get_text().strip())
# نظرًا لأن المستند يمتلك هذه الفقرة، يمكننا تطبيق أحد أنماطه على محتوى الفقرة.
para.paragraph_format.style = doc.styles.get_by_name('Heading 1')
# أضف هذه العقدة إلى المستند، ثم تحقق من محتوياتها.
doc.first_section.body.append_child(para)
self.assertEqual(doc.first_section.body, para.parent_node)
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Node](../)

