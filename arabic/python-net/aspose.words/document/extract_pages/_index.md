---
title: Document.extract_pages method
linktitle: extract_pages method
articleTitle: extract_pages method
second_title: Aspose.Words for Python
description: "aspose.words.Document.extract_pages method"
type: docs
weight: 650
url: /ar/python-net/aspose.words/document/extract_pages/
---

## extract_pages(index, count, options) {#int_int_pageextractoptions}

Returns the [Document](../) object representing the specified range of pages and the given page extract options.



```python
def extract_pages(self, index: int, count: int, options: aspose.words.PageExtractOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the first page to extract. |
| count | int | Number of pages to be extracted. |
| options | [PageExtractOptions](../../pageextractoptions/) | Provides options for managing the page extracting process. |

### Remarks

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' – the numbering,
headers/footers and cross tables layout will be preserved.
But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort.
Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document.
Any feedback would be greatly appreciated.


## extract_pages(index, count) {#int_int}

Returns the [Document](../) object representing specified range of pages.



```python
def extract_pages(self, index: int, count: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the first page to extract. |
| count | int | Number of pages to be extracted. |

### Remarks

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' – the numbering,
headers/footers and cross tables layout will be preserved.
But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort.
Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document.
Any feedback would be greatly appreciated.


## Examples

Shows how to get specified range of pages from the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Layout entities.docx')
doc = doc.extract_pages(index=0, count=2)
doc.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPages.docx')
```

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

## See Also

* module [aspose.words](../../)
* class [Document](../)

