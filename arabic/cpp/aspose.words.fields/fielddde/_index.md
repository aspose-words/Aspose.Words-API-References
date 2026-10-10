---
title: "Aspose::Words::Fields::FieldDde class"
linktitle: "FieldDde"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldDde class. ينفّذ حقل DDE. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words.fields/fielddde/
---
## FieldDde class


يطبق حقل DDE. لمعرفة المزيد، قم بزيارة [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldDde : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | يحصل على ما إذا كان يجب تحديث هذا الحقل تلقائيًا. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | يحصل على ما إذا كان سيتم إدراج الكائن المرتبط كصورة نقطية. |
| [get_InsertAsHtml](./get_insertashtml/)() | يحصل على ما إذا كان سيتم إدراج الكائن المرتبط كنص بتنسيق HTML. |
| [get_InsertAsPicture](./get_insertaspicture/)() | يحصل على ما إذا كان سيتم إدراج الكائن المرتبط كصورة. |
| [get_InsertAsRtf](./get_insertasrtf/)() | يحصل على ما إذا كان سيتم إدراج الكائن المرتبط بتنسيق النص الغني (RTF). |
| [get_InsertAsText](./get_insertastext/)() | يحصل على ما إذا كان سيتم إدراج الكائن المرتبط بتنسيق نص فقط. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | يحصل على ما إذا كان سيتم إدراج الكائن المرتبط كنص Unicode. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLinked](./get_islinked/)() | يحصل على ما إذا كان سيتم تقليل حجم الملف بعدم تخزين بيانات الرسومات مع المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_ProgId](./get_progid/)() | يحصل على نوع التطبيق لمعلومات الارتباط. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_SourceFullName](./get_sourcefullname/)() | يحصل على اسم وموقع ملف المصدر. |
| [get_SourceItem](./get_sourceitem/)() | يحصل على الجزء من ملف المصدر الذي يتم ربطه. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_AutoUpdate](./set_autoupdate/)(bool) | يضبط ما إذا كان سيتم تحديث هذا الحقل تلقائيًا. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | يضبط ما إذا كان سيتم إدراج الكائن المرتبط كصورة نقطية. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | يضبط ما إذا كان سيتم إدراج الكائن المرتبط كنص بتنسيق HTML. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | يضبط ما إذا كان سيتم إدراج الكائن المرتبط كصورة. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | يضبط ما إذا كان سيتم إدراج الكائن المرتبط بتنسيق النص الغني (RTF). |
| [set_InsertAsText](./set_insertastext/)(bool) | يضبط ما إذا كان سيتم إدراج الكائن المرتبط بتنسيق نص فقط. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | يضبط ما إذا كان سيتم إدراج الكائن المرتبط كنص Unicode. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | يضبط ما إذا كان سيتم تقليل حجم الملف بعدم تخزين بيانات الرسومات مع المستند. |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | يضبط نوع التطبيق لمعلومات الارتباط. |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | يضبط اسم وموقع ملف المصدر. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | يضبط الجزء من ملف المصدر الذي يتم ربطه. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
