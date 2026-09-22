---
title: "فئة Aspose::Words::Fields::FieldTA"
linktitle: "FieldTA"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldTA. تنفذ حقل TA. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 99000
url: /ar/cpp/aspose.words.fields/fieldta/
---
## FieldTA class


يُنفّذ الحقل TA. لتعلم المزيد، زر [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldTA : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_EntryCategory](./get_entrycategory/)() | يحصل على فئة الإدخال المتكاملة، وهي رقم يتطابق مع ترتيب الفئات. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsBold](./get_isbold/)() | يحصل على ما إذا كان يجب تطبيق تنسيق عريض على رقم الصفحة للإدخال. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsItalic](./get_isitalic/)() | يحصل على ما إذا كان يجب تطبيق تنسيق مائل على رقم الصفحة للإدخال. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_LongCitation](./get_longcitation/)() | يحصل على الاقتباس الطويل للمدخل. |
| [get_PageRangeBookmarkName](./get_pagerangebookmarkname/)() | يحصل على اسم الإشارة المرجعية التي تحدد نطاق الصفحات المُدرج كرقم صفحة للمدخل. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_ShortCitation](./get_shortcitation/)() | يحصل على الاقتباس القصير للمدخل. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | يضبط فئة المدخل المتكاملة، وهي رقم يتطابق مع ترتيب الفئات. |
| [set_IsBold](./set_isbold/)(bool) | يضبط ما إذا كان سيتم تطبيق تنسيق غامق على رقم الصفحة للمدخل. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsItalic](./set_isitalic/)(bool) | يضبط ما إذا كان سيتم تطبيق تنسيق مائل على رقم الصفحة للمدخل. |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LongCitation](./set_longcitation/)(const System::String\&) | يضبط الاقتباس الطويل للمدخل. |
| [set_PageRangeBookmarkName](./set_pagerangebookmarkname/)(const System::String\&) | يضبط اسم الإشارة المرجعية التي تحدد نطاق الصفحات المُدرج كرقم صفحة للمدخل. |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ShortCitation](./set_shortcitation/)(const System::String\&) | يضبط الاقتباس القصير للمدخل. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
