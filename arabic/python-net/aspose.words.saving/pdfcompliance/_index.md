---
title: PdfCompliance enumeration
linktitle: PdfCompliance enumeration
articleTitle: PdfCompliance enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfCompliance enumeration. Specifies the PDF standards compliance level."
type: docs
weight: 630
url: /ar/python-net/aspose.words.saving/pdfcompliance/
---

## PdfCompliance enumeration

Specifies the PDF standards compliance level.


### Members

| Name | Description |
| --- | --- |
| PDF17 | The output file will comply with the PDF 1.7 (ISO 32000-1) standard. |
| PDF20 | The output file will comply with the PDF 2.0 (ISO 32000-2) standard. |
| PDF_A1A | The output file will comply with the PDF/A-1a (ISO 19005-1) standard. This level includes all the requirements of PDF/A-1b and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. |
| PDF_A1B | The output file will comply with the PDF/A-1b (ISO 19005-1) standard. PDF/A-1b has the objective of ensuring reliable reproduction of the visual appearance of the document. |
| PDF_A2A | The output file will comply with the PDF/A-2a (ISO 19005-2) standard. This level includes all the requirements of PDF/A-2u and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. |
| PDF_A2U | The output file will comply with the PDF/A-2u (ISO 19005-2) standard. PDF/A-2u has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally, any text contained in the document can be reliably extracted as a series of Unicode codepoints. |
| PDF_A3A | The output file will comply with the PDF/A-3a (ISO 19005-3) standard. This level includes all the requirements of PDF/A-3u and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. |
| PDF_A3U | The output file will comply with the PDF/A-3u (ISO 19005-3) standard. PDF/A-3u (as well as PDF/A-2u) has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally, any text contained in the document can be reliably extracted as a series of Unicode codepoints. In addition to PDF/A-2u, PDF/A-3u allows embedding attachments to the PDF document. |
| PDF_A4 | The output file will comply with the PDF/A-4 (ISO 19005-4:2020) standard. PDF/A-4 has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally, any text contained in the document can be reliably extracted as a series of Unicode codepoints. |
| PDF_A4F | The output file will comply with the PDF/A-4f (ISO 19005-4:2020) standard. This level includes all the requirements of PDF/A-4 and additionally allows embedding attachments to the PDF document. |
| PDF_A4_UA_2 | The output file will comply with both PDF/A-4 (ISO 19005-4:2020) and PDF/UA-2 (ISO 14289-2:2024) standards. PDF/A-4 has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible. |
| PDF_UA1 | The output file will comply with the PDF/UA-1 (ISO 14289-1) standard. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible. |
| PDF_UA2 | The output file will comply with the PDF/UA-2 (ISO 14289-2:2024) standard. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible. |

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

* module [aspose.words.saving](../)

