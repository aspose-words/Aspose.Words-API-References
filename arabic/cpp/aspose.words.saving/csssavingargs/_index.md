---
title: "Aspose::Words::Saving::CssSavingArgs class"
linktitle: "CssSavingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::CssSavingArgs class. يوفر البيانات لحدث CssSaving(). لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


يوفر البيانات لحدث [CssSaving()](../icsssavingcallback/csssaving/). لمعرفة المزيد، زر مقالة الوثائق [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class CssSavingArgs : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | يسمح بتحديد الدفق الذي سيتم حفظ معلومات CSS إليه. |
| [get_Document](./get_document/)() const | يحصل على كائن المستند الذي يتم حفظه حاليًا. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف وتضمينه في مستند HTML. القيمة الافتراضية هي **true**. عندما تكون هذه الخاصية **false**، لن يتم حفظ معلومات CSS في ملف CSS ولن يتم تضمينه في مستند HTML. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | يحدد ما إذا كان Aspose.Words يجب أن يبقي الدفق مفتوحًا أو يغلقه بعد حفظ معلومات CSS. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | محدد لـ [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف وتضمينه في مستند HTML. القيمة الافتراضية هي **true**. عندما تكون هذه الخاصية **false**، لن يتم حفظ معلومات CSS في ملف CSS ولن يتم تضمينه في مستند HTML. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | محدد لـ [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |
| static [Type](./type/)() |  |
## ملاحظات


بشكل افتراضي، عندما يقوم Aspose.Words بحفظ مستند إلى HTML، يحفظ معلومات CSS مضمّنًا (كقيمة لخاصية **style** على كل عنصر).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

لحفظ CSS في الدفق، استخدم الخاصية [CssStream](./get_cssstream/).

لمنع حفظ CSS في ملف وتضمينه في مستند HTML استخدم الخاصية [IsExportNeeded](./get_isexportneeded/).
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
