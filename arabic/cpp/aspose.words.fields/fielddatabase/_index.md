---
title: "Aspose::Words::Fields::FieldDatabase فئة"
linktitle: "FieldDatabase"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldDatabase فئة. تنفذ حقل DATABASE. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 28000
url: /ar/cpp/aspose.words.fields/fielddatabase/
---
## FieldDatabase class


يُنفّذ حقل DATABASE. لمزيد من المعلومات، زر [العمل مع الحقول](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldDatabase : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [FieldDatabase](./fielddatabase/)() |  |
| [get_Connection](./get_connection/)() | يحصل على اتصال بالبيانات. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_FileName](./get_filename/)() | يحصل على المسار الكامل واسم الملف لقاعدة البيانات. |
| [get_FirstRecord](./get_firstrecord/)() | يحصل على رقم السجل الكامل للسجل البيانات الأول لإدراجه. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_FormatAttributes](./get_formatattributes/)() | يحصل على أي سمات التنسيق التي سيتم تطبيقها على الجدول. |
| [get_InsertHeadings](./get_insertheadings/)() | يحصل على ما إذا كان سيتم إدراج أسماء الحقول من قاعدة البيانات كعناوين أعمدة في الجدول الناتج. |
| [get_InsertOnceOnMailMerge](./get_insertonceonmailmerge/)() | يحصل على ما إذا كان سيتم إدراج البيانات في بداية الدمج. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LastRecord](./get_lastrecord/)() | يحصل على رقم السجل الكامل للسجل البيانات الأخير لإدراجه. |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_Query](./get_query/)() | يحصل على مجموعة من تعليمات SQL التي تستعلم قاعدة البيانات. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_TableFormat](./get_tableformat/)() | يحصل على التنسيق الذي سيُطبق على نتيجة استعلام قاعدة البيانات. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_Connection](./set_connection/)(const System::String\&) | يضبط اتصالًا بالبيانات. |
| [set_FileName](./set_filename/)(const System::String\&) | يضبط المسار الكامل واسم الملف لقاعدة البيانات. |
| [set_FirstRecord](./set_firstrecord/)(const System::String\&) | يضبط رقم السجل الكامل للسجل البيانات الأول لإدراجه. |
| [set_FormatAttributes](./set_formatattributes/)(const System::String\&) | يضبط أي سمات التنسيق التي سيتم تطبيقها على الجدول. |
| [set_InsertHeadings](./set_insertheadings/)(bool) | يضبط ما إذا كان سيتم إدراج أسماء الحقول من قاعدة البيانات كعناوين أعمدة في الجدول الناتج. |
| [set_InsertOnceOnMailMerge](./set_insertonceonmailmerge/)(bool) | يضبط ما إذا كان سيتم إدراج البيانات في بداية الدمج. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LastRecord](./set_lastrecord/)(const System::String\&) | يضبط رقم السجل الكامل للسجل البيانات الأخير لإدراجه. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Query](./set_query/)(const System::String\&) | يضبط مجموعة من تعليمات SQL التي تستعلم قاعدة البيانات. |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TableFormat](./set_tableformat/)(const System::String\&) | يضبط التنسيق الذي سيُطبق على نتيجة استعلام قاعدة البيانات. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
