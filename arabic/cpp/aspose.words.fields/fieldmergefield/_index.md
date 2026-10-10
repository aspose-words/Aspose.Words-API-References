---
title: "فئة Aspose::Words::Fields::FieldMergeField"
linktitle: "FieldMergeField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldMergeField. تنفذ الحقل MERGEFIELD. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 67000
url: /ar/cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


ينفذ حقل MERGEFIELD. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field,
                        public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldName](./get_fieldname/)() | يحصل على اسم حقل بيانات. |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | يرجع فقط اسم حقل البيانات. يتم إزالة أي بادئة إلى خاصية البادئة. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_IsMapped](./get_ismapped/)() | يحصل على ما إذا كان هذا الحقل حقلًا مخططًا. |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | يحصل على ما إذا كان يجب تمكين تحويل الأحرف للتنسيق العمودي. |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_TextAfter](./get_textafter/)() | يحصل على النص الذي سيُدرج بعد الحقل إذا لم يكن الحقل فارغًا. |
| [get_TextBefore](./get_textbefore/)() | يحصل على النص الذي سيُدرج قبل الحقل إذا لم يكن الحقل فارغًا. |
| [get_Type](./get_type/)() const override | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_FieldName](./set_fieldname/)(const System::String\&) | يضبط اسم حقل بيانات. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsMapped](./set_ismapped/)(bool) | يضبط ما إذا كان هذا الحقل حقلًا مخططًا. |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | يضبط ما إذا كان يجب تمكين تحويل الأحرف للتنسيق العمودي. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TextAfter](./set_textafter/)(const System::String\&) | يضبط النص الذي سيُدرج بعد الحقل إذا لم يكن الحقل فارغًا. |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | يضبط النص الذي سيُدرج قبل الحقل إذا لم يكن الحقل فارغًا. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
