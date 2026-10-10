---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName. تحدد ما إذا كان سيتم استخدام خاصية Tag أو Id لعنصر التحكم SDT كاسم لحقل النموذج في PDF في C++."
type: docs
weight: 32500
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


يحدد ما إذا كان يجب استخدام خاصية Tag أو Id في عنصر التحكم SDT كاسم لحقل النموذج في PDF.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## ملاحظات


القيمة الافتراضية هي **false**.

عند تعيينه إلى **false**، يتم استخدام خاصية Id لعنصر التحكم SDT كاسم لحقل النموذج في PDF.

عند تعيينه إلى **true**، يتم استخدام خاصية Tag لعنصر التحكم SDT كاسم لحقل النموذج في PDF.

إذا تم تعيينه إلى **true** وكانت الخاصية Tag فارغة، سيتم استخدام خاصية Id كاسم لحقل النموذج.

إذا تم تعيينه إلى **true** وكانت قيم Tag غير فريدة، سيتم تعديل قيم Tag المكررة لإنشاء أسماء فريدة لحقول نموذج PDF.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
