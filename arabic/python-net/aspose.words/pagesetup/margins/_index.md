---
title: PageSetup.margins property
linktitle: margins property
articleTitle: margins property
second_title: Aspose.Words for Python
description: "PageSetup.margins property. Returns or sets preset [Margins](../../margins/) of the page."
type: docs
weight: 260
url: /ar/python-net/aspose.words/pagesetup/margins/
---

## PageSetup.margins property

Returns or sets preset [Margins](../../margins/) of the page.



```python
@property
def margins(self) -> aspose.words.Margins:
    ...

@margins.setter
def margins(self, value: aspose.words.Margins):
    ...

```

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

* module [aspose.words](../../)
* class [PageSetup](../)

