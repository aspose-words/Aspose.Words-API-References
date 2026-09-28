---
title: PageExtractOptions.update_page_starting_number property
linktitle: update_page_starting_number property
articleTitle: update_page_starting_number property
second_title: Aspose.Words for Python
description: "PageExtractOptions.update_page_starting_number property. Specifies whether the start page number in the resulting document shall be updated"
type: docs
weight: 30
url: /ar/python-net/aspose.words/pageextractoptions/update_page_starting_number/
---

## PageExtractOptions.update_page_starting_number property

Specifies whether the start page number in the resulting document shall be updated.
Default value is ``True``.



```python
@property
def update_page_starting_number(self) -> bool:
    ...

@update_page_starting_number.setter
def update_page_starting_number(self, value: bool):
    ...

```

### Examples

Show how to reset the initial page numbering and save the NUMPAGE field.

```python
doc = aw.Document(file_name=MY_DIR + 'Page fields.docx')
# السلوك الافتراضي:
# ترقيم الصفحات المستخرج هو نفسه كما في الوثيقة الأصلية، كما لو أننا اخترنا \"Print 2 pages\" في MS Word.
# سيتم تعيين صفحة البداية إلى 2 وسيتم إزالة الحقل الذي يشير إلى عدد الصفحات
# ويستبدل بقيمة ثابتة مساوية لعدد الصفحات.
extracted_doc1 = doc.extract_pages(index=1, count=1)
extracted_doc1.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Default.docx')
# السلوك المعدل:
# ترقيم الصفحات المستخرج يُعاد ضبطه ويبدأ ترقيم جديد،
# كما لو أننا نسخنا محتويات الصفحة الثانية ولصقناها في وثيقة جديدة.
# سيتم تعيين صفحة البداية إلى 1 وسيُترك الحقل الذي يشير إلى عدد الصفحات دون تغيير
# وسيظهر عدد الصفحات الحالي.
extract_options = aw.PageExtractOptions()
extract_options.update_page_starting_number = False
extract_options.unlink_pages_number_fields = False
extracted_doc2 = doc.extract_pages(index=1, count=1, options=extract_options)
extracted_doc2.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Options.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageExtractOptions](../)

