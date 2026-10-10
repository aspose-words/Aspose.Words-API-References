---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream طريقة"
linktitle: "get_CssStream"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream طريقة. يسمح بتحديد الدفق الذي سيتم حفظ معلومات CSS فيه في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


يسمح بتحديد الدفق الذي سيتم حفظ معلومات CSS إليه.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## ملاحظات


هذه الخاصية تسمح لك بحفظ معلومات CSS إلى تدفق.

القيمة الافتراضية هي **null**. هذه الخاصية لا تمنع حفظ معلومات CSS إلى ملف أو تضمينها في مستند HTML. لمنع تصدير CSS استخدم الخاصية [IsExportNeeded](../get_isexportneeded/).

باستخدام [ICssSavingCallback](../../icsssavingcallback/) لا يمكنك استبدال CSS بآخر. إنها مخصصة فقط لحفظ CSS إلى تدفق.

## انظر أيضًا

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
