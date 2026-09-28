---
title: Document.page_count property
linktitle: page_count property
articleTitle: page_count property
second_title: Aspose.Words for Python
description: "Document.page_count property. Gets the number of pages in the document as calculated by the most recent page layout operation."
type: docs
weight: 330
url: /ar/python-net/aspose.words/document/page_count/
---

## Document.page_count property

Gets the number of pages in the document as calculated by the most recent page layout operation.


```python
@property
def page_count(self) -> int:
    ...

```

### Examples

Shows how to count the number of pages in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Page 3')
# تحقق من عدد الصفحات المتوقع للمستند.
self.assertEqual(3, doc.page_count)
# استدعاء خاصية PageCount فعل تخطيط صفحات المستند لحساب القيمة.
# لن تحتاج هذه العملية إلى إعادة تنفيذها عند تحويل المستند إلى تنسيق حفظ صفحة ثابت،
# مثل .pdf. لذا يمكنك توفير بعض الوقت، خاصةً مع المستندات الأكثر تعقيدًا.
doc.save(file_name=ARTIFACTS_DIR + 'Document.GetPageCount.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)
* method [Document.update_page_layout()](../update_page_layout/#default)

