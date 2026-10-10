---
title: PdfSaveOptions.export_document_structure property
linktitle: export_document_structure property
articleTitle: export_document_structure property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.export_document_structure property. Gets or sets a value determining whether or not to export document structure."
type: docs
weight: 140
url: /ar/python-net/aspose.words.saving/pdfsaveoptions/export_document_structure/
---

## PdfSaveOptions.export_document_structure property

Gets or sets a value determining whether or not to export document structure.


```python
@property
def export_document_structure(self) -> bool:
    ...

@export_document_structure.setter
def export_document_structure(self, value: bool):
    ...

```

### Remarks

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially
for the large documents.




### Examples

Shows how to preserve document structure elements, which can assist in programmatically interpreting our document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# اضبط الخاصية "ExportDocumentStructure" إلى "true" لجعل بنية المستند، مثل هذه الوسوم، متاحة عبر الـ
# "Content" لوحة التنقل في Adobe Acrobat على حساب زيادة حجم الملف.
# اضبط الخاصية "ExportDocumentStructure" إلى "false" لعدم تصدير بنية المستند.
options.export_document_structure = export_document_structure
# افترض أننا نقوم بتصدير بنية المستند أثناء حفظ هذا المستند. في هذه الحالة،
# يمكننا فتحه باستخدام Adobe Acrobat والعثور على وسوم للعناصر مثل العنوان
# والفقرة التالية عبر "View" -> "Show/Hide" -> "Navigation panes" -> "Tags".
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportDocumentStructure.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

