---
title: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded طريقة"
linktitle: "get_IsSubsettingNeeded"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded. تسمح بتحديد ما إذا كان سيتم تقليص الخط الحالي قبل تصديره كموارد خط في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


يسمح بتحديد ما إذا كان الخط الحالي سيُقسم إلى مجموعة فرعية قبل تصديره كموارد خط.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## ملاحظات


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

بشكل افتراضي، يقرر Aspose.Words ما إذا كان سيجري تقليص الخط أم لا عن طريق مقارنة حجم ملف الخط الأصلي مع الحجم المحدد في [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/). يمكنك تجاوز هذا السلوك للخطوط الفردية عن طريق ضبط خاصية [IsSubsettingNeeded](./).
## انظر أيضًا

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
