---
title: PdfSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.compliance property. Specifies the PDF standards compliance level for output documents."
type: docs
weight: 50
url: /ar/python-net/aspose.words.saving/pdfsaveoptions/compliance/
---

## PdfSaveOptions.compliance property

Specifies the PDF standards compliance level for output documents.


```python
@property
def compliance(self) -> aspose.words.saving.PdfCompliance:
    ...

@compliance.setter
def compliance(self, value: aspose.words.saving.PdfCompliance):
    ...

```

### Remarks

Default is [PdfCompliance.PDF17](../../pdfcompliance/#PDF17).




### Examples

Shows how to set the PDF standards compliance level of saved PDF documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
# لاحظ أن بعض PdfSaveOptions محظورة عند الحفظ إلى أحد المعايير ويتم إصلاحها تلقائيًا.
# استخدم IWarningCallback لمعرفة الخيارات التي تم إصلاحها تلقائيًا.
save_options = aw.saving.PdfSaveOptions()
# اضبط الخاصية "Compliance" إلى "PdfCompliance.PdfA1b" للامتثال للمعيار "PDF/A-1b"،
# الذي يهدف إلى الحفاظ على المظهر البصري للمستند كما يقوم Aspose.Words بتحويله إلى PDF.
# اضبط الخاصية "Compliance" إلى "PdfCompliance.Pdf17" للامتثال للمعيار "1.7".
# اضبط خاصية "Compliance" إلى "PdfCompliance.PdfA1a" للامتثال للمعيار "PDF/A-1a",
# التي تتوافق مع "PDF/A-1b" بالإضافة إلى الحفاظ على بنية المستند الأصلي.
# اضبط خاصية "Compliance" إلى "PdfCompliance.PdfUa1" للامتثال للمعيار "PDF/UA-1" (ISO 14289-1),
# التي تهدف إلى تعريف تمثيل المستندات الإلكترونية في PDF التي تسمح بإمكانية الوصول إلى الملف.
# اضبط خاصية "Compliance" إلى "PdfCompliance.Pdf20" للامتثال للمعيار "PDF 2.0" (ISO 32000-2).
# اضبط خاصية "Compliance" إلى "PdfCompliance.PdfA4" للامتثال للمعيار "PDF/A-4" (ISO 19004:2020),
# التي تحافظ على المظهر البصري الثابت للمستند مع مرور الوقت.
# اضبط خاصية "Compliance" إلى "PdfCompliance.PdfA4Ua2" للامتثال لكل من PDF/A-4 (ISO 19005-4:2020)
# و معايير PDF/UA-2 (ISO 14289-2:2024).
# اضبط خاصية "Compliance" إلى "PdfCompliance.PdfUa2" للامتثال للمعيار PDF/UA-2 (ISO 14289-2:2024).
# هذا يساعد في جعل المستندات قابلة للبحث ولكن قد يزيد بشكل كبير من حجم المستندات الكبيرة بالفعل.
save_options.compliance = pdf_compliance
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.Compliance.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

