---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields"
linktitle: "get_PreserveFormFields"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields. تحدد ما إذا كان سيتم الحفاظ على حقول نموذج Microsoft Word كحقول نموذج في PDF أو تحويلها إلى نص. القيمة الافتراضية هي false في C++."
type: docs
weight: 28000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


يحدد ما إذا كان يجب الحفاظ على حقول نماذج Microsoft Word كحقول نماذج في PDF أو تحويلها إلى نص. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## ملاحظات


تشمل حقول نموذج Microsoft Word إدخالات نصية، وقوائم منسدلة، وعناصر تحكم مربعات اختيار.

عند تعيينها إلى **false**، سيتم تصدير هذه الحقول كنص إلى PDF. وعند تعيينها إلى **true**، سيتم تصدير هذه الحقول كحقول نموذج PDF.

عند تصدير حقول النموذج إلى PDF كحقول نموذج، قد يحدث فقدان بعض التنسيق لأن حقول نموذج PDF لا تدعم جميع ميزات حقول نموذج Microsoft Word.

أيضًا، يعتمد حجم الإخراج على حجم المحتوى لأن النماذج القابلة للتحرير في Microsoft Word هي كائنات مضمنة.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
