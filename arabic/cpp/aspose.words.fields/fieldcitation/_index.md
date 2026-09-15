---
title: "Aspose::Words::Fields::FieldCitation فئة"
linktitle: "FieldCitation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldCitation فئة. يُنفّذ حقل CITATION. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


يُنفّذ حقل CITATION. لمزيد من المعلومات، زر [العمل مع الحقول](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | يحصل على قيمة تتطابق مع قيمة عنصر **Tag** لمصدر آخر لتضمينه في الاقتباس. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | يحصل على معرف اللغة المستخدم بالاشتراك مع النمط الببليوغرافي المحدد لتنسيق الاقتباس في المستند. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_PageNumber](./get_pagenumber/)() | يحصل على رقم صفحة مرتبط بالاقتباس. |
| [get_Prefix](./get_prefix/)() | يحصل على بادئة تُضاف إلى بداية الاقتباس. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_SourceTag](./get_sourcetag/)() | يحصل على قيمة تتطابق مع قيمة عنصر **Tag** للمصدر المراد إدراجه. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Suffix](./get_suffix/)() | يحصل على لاحقة تُضاف إلى نهاية الاقتباس. |
| [get_SuppressAuthor](./get_suppressauthor/)() | يحصل على ما إذا كان يتم إخفاء معلومات المؤلف من الاقتباس. |
| [get_SuppressTitle](./get_suppresstitle/)() | يحصل على ما إذا كان يتم إخفاء معلومات العنوان من الاقتباس. |
| [get_SuppressYear](./get_suppressyear/)() | يحصل على ما إذا كان يتم إخفاء معلومات السنة من الاقتباس. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [get_VolumeNumber](./get_volumenumber/)() | يحصل على رقم المجلد المرتبط بالاقتباس. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | يضبط قيمة تتطابق مع قيمة عنصر **Tag** لمصدر آخر لتضمينه في الاقتباس. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | يضبط معرف اللغة المستخدم بالاشتراك مع النمط الببليوغرافي المحدد لتنسيق الاقتباس في المستند. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | يضبط رقم صفحة مرتبط بالاقتباس. |
| [set_Prefix](./set_prefix/)(const System::String\&) | يضبط بادئة تُضاف إلى بداية الاقتباس. |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | يضبط قيمة تتطابق مع قيمة عنصر **Tag** للمصدر المراد إدراجه. |
| [set_Suffix](./set_suffix/)(const System::String\&) | يضبط لاحقة تُضاف إلى نهاية الاقتباس. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | يضبط ما إذا كان يتم إخفاء معلومات المؤلف من الاقتباس. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | يضبط ما إذا كان يتم إخفاء معلومات العنوان من الاقتباس. |
| [set_SuppressYear](./set_suppressyear/)(bool) | يضبط ما إذا كان يتم إخفاء معلومات السنة من الاقتباس. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | يضبط رقم المجلد المرتبط بالاقتباس. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
