---
title: Document.update_page_layout method
linktitle: update_page_layout method
articleTitle: update_page_layout method
second_title: Aspose.Words for Python
description: "Document.update_page_layout method. Rebuilds the page layout of the document."
type: docs
weight: 820
url: /ar/python-net/aspose.words/document/update_page_layout/
---

## update_page_layout() {#default}

Rebuilds the page layout of the document.


```python
def update_page_layout(self):
    ...
```

### Remarks

This method formats a document into pages and updates the page number related fields in the document such
as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document
to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it.
However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not
update the page layout automatically. In this case you should call [Document.update_page_layout()](./#default) before
rendering again.




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
* class [Document](../)

