---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression"
linktitle: "get_ImageCompression"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression. تحدد نوع الضغط الذي سيُستخدم لجميع الصور في المستند في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions::get_ImageCompression method


يحدد نوع الضغط الذي سيُستخدم لجميع الصور في المستند.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```

## ملاحظات


القيمة الافتراضية هي [Auto](../../pdfimagecompression/).

استخدام [Jpeg](../../pdfimagecompression/) يتيح لك التحكم في جودة الصور في المستند الناتج عبر خاصية [JpegQuality](../get_jpegquality/).

استخدام [Jpeg](../../pdfimagecompression/) يوفر أسرع سرعة تحويل مقارنةً بأداء أنواع الضغط الأخرى، لكن في هذه الحالة يكون الضغط بصيغة JPEG بفقدان الجودة.

استخدام [Auto](../../pdfimagecompression/) يتيح التحكم في جودة JPEG في المستند الناتج عبر خاصية [JpegQuality](../get_jpegquality/)، ولكن بالنسبة للصيغ الأخرى يتم استخراج بيانات البكسل الخام وحفظها بضغط Flate. هذه الحالة أبطأ من تحويل JPEG لكنها بدون فقدان للجودة.
## انظر أيضًا

* Enum [PdfImageCompression](../../pdfimagecompression/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
