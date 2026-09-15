---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality"
linktitle: "get_JpegQuality"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality. تحصل أو تضبط قيمة تحدد جودة صور JPEG داخل مستند PDF في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_jpegquality/
---
## PdfSaveOptions::get_JpegQuality method


يحصل أو يضبط قيمة تحدد جودة صور JPEG داخل مستند PDF.

```cpp
int32_t Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality()
```

## ملاحظات


القيمة الافتراضية هي 100.

يتم استخدام هذه الخاصية بالتزامن مع خيار [ImageCompression](../get_imagecompression/).

يكون له تأثير فقط عندما يحتوي المستند على صور JPEG.

استخدم هذه الخاصية للحصول على أو ضبط جودة الصور داخل المستند عند الحفظ بصيغة PDF. يمكن أن تتراوح القيمة من 0 إلى 100 حيث يعني 0 أسوأ جودة ولكن أقصى ضغط و100 يعني أفضل جودة ولكن أقل ضغط. إذا كانت الجودة 100 وكانت الصورة الأصلية JPEG، فهذا يعني عدم وجود ضغط - سيتم حفظ البايتات الأصلية.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
