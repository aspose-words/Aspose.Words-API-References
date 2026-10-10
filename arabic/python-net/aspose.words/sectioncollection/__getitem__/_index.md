---
title: SectionCollection indexer
linktitle: SectionCollection indexer
articleTitle: SectionCollection indexer
second_title: Aspose.Words for Python
description: "SectionCollection indexer. Retrieves a section at the given index."
type: docs
weight: 10
url: /ar/python-net/aspose.words/sectioncollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a section at the given index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows when to recalculate the page layout of the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# حفظ المستند إلى PDF أو إلى صورة أو طباعته للمرة الأولى سيؤدي تلقائيًا إلى
# تخزين تخطيط المستند في ذاكرة التخزين المؤقت داخل صفحاته.
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.1.pdf')
# تعديل المستند بطريقة ما.
doc.styles.get_by_name('Normal').font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED
# في الإصدار الحالي من Aspose.Words، تعديل المستند لا يعيد بناء التخطيط المخزن مؤقتًا تلقائيًا
# تخطيط الصفحة المخزن مؤقتًا. إذا أردنا أن يبقى التخطيط المخزن مؤقتًا
# محدّثًا، سيتعين علينا تحديثه يدويًا.
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Document.UpdatePageLayout.2.pdf')
```

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
* class [SectionCollection](../)

