---
title: Section.ensure_minimum method
linktitle: ensure_minimum method
articleTitle: ensure_minimum method
second_title: Aspose.Words for Python
description: "Section.ensure_minimum method. Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/)."
type: docs
weight: 130
url: /ar/python-net/aspose.words/section/ensure_minimum/
---

## ensure_minimum() {#default}

Ensures that the section has [Section.body](../body/) with one [Paragraph](../../paragraph/).



```python
def ensure_minimum(self):
    ...
```

### Examples

Shows how to prepare a new section node for editing.

```python
doc = aw.Document()
# يأتي مستند فارغ مع قسم، يحتوي على جسم، والذي بدوره يحتوي على فقرة.
# يمكننا إضافة محتوى إلى هذا المستند عن طريق إضافة عناصر مثل مقاطع النص، أو الأشكال، أو الجداول إلى تلك الفقرة.
self.assertEqual(aw.NodeType.SECTION, doc.get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.BODY, doc.sections[0].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[0].body.get_child(aw.NodeType.ANY, 0, True).node_type)
# إذا أضفنا قسماً جديداً مثل هذا، فلن يحتوي على جسم، أو أي عقد فرعية أخرى.
doc.sections.add(aw.Section(doc))
self.assertEqual(0, doc.sections[1].get_child_nodes(aw.NodeType.ANY, True).count)
# قم بتشغيل الطريقة "EnsureMinimum" لإضافة جسم وفقرة إلى هذا القسم لبدء تحريره.
doc.last_section.ensure_minimum()
self.assertEqual(aw.NodeType.BODY, doc.sections[1].get_child(aw.NodeType.ANY, 0, True).node_type)
self.assertEqual(aw.NodeType.PARAGRAPH, doc.sections[1].body.get_child(aw.NodeType.ANY, 0, True).node_type)
doc.sections[0].body.first_paragraph.append_child(aw.Run(doc=doc, text='Hello world!'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

