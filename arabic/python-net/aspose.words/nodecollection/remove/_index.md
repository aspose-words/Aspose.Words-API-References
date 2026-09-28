---
title: NodeCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "NodeCollection.remove method. Removes the node from the collection and from the document."
type: docs
weight: 80
url: /ar/python-net/aspose.words/nodecollection/remove/
---

## remove(node) {#node}

Removes the node from the collection and from the document.


```python
def remove(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node to remove. |

### Examples

Shows how to work with a NodeCollection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أضف نصًا إلى المستند عن طريق إدراج Runs باستخدام DocumentBuilder.
builder.write('Run 1. ')
builder.write('Run 2. ')
# كل استدعاء لطريقة "Write" ينشئ Run جديد،
# والذي يظهر بعد ذلك في RunCollection الخاص بالفقرة الأب Paragraph.
runs = doc.first_section.body.first_paragraph.runs
self.assertEqual(2, runs.count)
# يمكننا أيضًا إدراج عقدة في RunCollection يدويًا.
new_run = aw.Run(doc=doc, text='Run 3. ')
runs.insert(3, new_run)
self.assertTrue(runs.contains(new_run))
self.assertEqual('Run 1. Run 2. Run 3.', doc.get_text().strip())
# الوصول إلى runs الفردية وإزالتها لإزالة نصها من المستند.
run = runs[1]
runs.remove(run)
self.assertEqual('Run 1. Run 3.', doc.get_text().strip())
self.assertIsNotNone(run)
self.assertFalse(runs.contains(run))
```

### See Also

* module [aspose.words](../../)
* class [NodeCollection](../)

