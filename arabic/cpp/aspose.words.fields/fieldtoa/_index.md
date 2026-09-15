---
title: "Aspose::Words::Fields::FieldToa فئة"
linktitle: "FieldToa"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldToa. تنفذ حقل TOA. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 104000
url: /ar/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


يُنفّذ الحقل TOA. لتعلم المزيد، زر [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | يحصل على اسم العلامة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الجدول. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_EntryCategory](./get_entrycategory/)() | يحصل على الفئة الكاملة للمدخلات المشمولة في الجدول. |
| [get_EntrySeparator](./get_entryseparator/)() | يحصل على تسلسل الأحرف المستخدم لفصل مدخل جدول المراجع ورقم صفحته. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | يحصل على تسلسل الأحرف المستخدم لفصل رقمين صفحتين في قائمة أرقام الصفحات. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | يحصل على تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحات. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | يحصل على ما إذا كان يجب إزالة تنسيق نص المدخل في المستند من المدخل في جدول المراجع. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_SequenceName](./get_sequencename/)() | يحصل على اسم تسلسل يُدرج رقمه مع رقم الصفحة. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | يحصل على تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [get_UseHeading](./get_useheading/)() | يحصل على ما إذا كان يجب تضمين عنوان الفئة للمدخلات في جدول المراجع. |
| [get_UsePassim](./get_usepassim/)() | يحصل على ما إذا كان يجب استبدال خمس أو أكثر من الإشارات الصفحية المختلفة لنفس المرجع بـ "passim"، والذي يُستخدم للدلالة على أن كلمة أو مقطع يظهر بشكل متكرر في العمل المستشهد به. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | يضبط اسم العلامة المرجعية التي تحدد الجزء من المستند المستخدم لبناء الجدول. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | يضبط الفئة الكاملة للمدخلات المشمولة في الجدول. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | يضبط تسلسل الأحرف المستخدم لفصل مدخل جدول المراجع ورقم صفحته. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | يضبط تسلسل الأحرف المستخدم لفصل رقمين صفحتين في قائمة أرقام الصفحات. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | يضبط تسلسل الأحرف المستخدم لفصل بداية ونهاية نطاق الصفحات. |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | يضبط ما إذا كان يجب إزالة تنسيق نص المدخل في المستند من المدخل في جدول المراجع. |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | يضبط اسم تسلسل يُدرج رقمه مع رقم الصفحة. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | يضبط تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [set_UseHeading](./set_useheading/)(bool) | يضبط ما إذا كان يجب تضمين عنوان الفئة للمدخلات في جدول المراجع. |
| [set_UsePassim](./set_usepassim/)(bool) | يضبط ما إذا كان سيتم استبدال خمس أو أكثر من الإشارات الصفحية المختلفة إلى نفس المرجع بـ "passim"، والذي يُستخدم للدلالة على أن كلمة أو مقطع يظهر بشكل متكرر في العمل المستشهد به. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
