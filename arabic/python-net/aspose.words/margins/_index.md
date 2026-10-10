---
title: Margins enumeration
linktitle: Margins enumeration
articleTitle: Margins enumeration
second_title: Aspose.Words for Python
description: "aspose.words.Margins enumeration. Specifies preset margins."
type: docs
weight: 760
url: /ar/python-net/aspose.words/margins/
---

## Margins enumeration

Specifies preset margins.


### Members

| Name | Description |
| --- | --- |
| NORMAL | Normal margins. |
| NARROW | Narrow margins. |
| MODERATE | Moderate margins. |
| WIDE | Wide margins. |
| MIRRORED | Mirrored margins. |
| CUSTOM | Custom margins. |

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

### See Also

* module [aspose.words](../)

