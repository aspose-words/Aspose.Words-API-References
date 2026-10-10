---
title: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode طريقة"
linktitle: "get_ImageColorSpaceExportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode طريقة. يحدد كيفية اختيار مساحة اللون للصور في مستند PDF بلغة C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


يحدد كيفية اختيار مساحة اللون للصور في مستند PDF.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## ملاحظات


القيمة الافتراضية هي [Auto](../../pdfimagecolorspaceexportmode/).

إذا تم تحديد قيمة [SimpleCmyk](../../pdfimagecolorspaceexportmode/)، يتم تجاهل خيار [ImageCompression](../get_imagecompression/) ويُستخدم ضغط Flate لجميع الصور في المستند.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead. 
## انظر أيضًا

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
