---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails"
linktitle: "get_EncryptionDetails"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails method. يحصل أو يضبط التفاصيل لتشفير مستند PDF الناتج في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_encryptiondetails/
---
## PdfSaveOptions::get_EncryptionDetails method


يحصل أو يضبط تفاصيل تشفير مستند PDF الناتج.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfEncryptionDetails> Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails() const
```

## ملاحظات


القيمة الافتراضية هي **null** ولن يتم تشفير المستند الناتج. عندما يتم تعيين هذه الخاصية إلى كائن [PdfEncryptionDetails](../../pdfencryptiondetails/) صالح، سيتم تشفير مستند PDF الناتج.

يتم استخدام خوارزمية التشفير AES-128 عند الحفظ وفقًا للامتثال PDF 1.7 (بما في ذلك PDF/UA-1). يتم استخدام خوارزمية التشفير AES-256 عند الحفظ وفقًا للامتثال PDF 2.0.

يُحظر التشفير وفقًا لامتثال PDF/A. سيتم تجاهل هذا الخيار عند الحفظ إلى PDF/A.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[ContentCopyForAccessibility](../../pdfpermissions/) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0. 
## انظر أيضًا

* Class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
