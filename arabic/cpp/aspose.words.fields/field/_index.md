---
title: "Aspose::Words::Fields::Field class"
linktitle: "حقل"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::Field class. يمثل حقلًا في مستند Microsoft Word. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fields/field/
---
## Field class


يمثل حقل مستند Microsoft Word. لمعرفة المزيد، زر مقالة الوثائق.

```cpp
class Field : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](./get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](./get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](./get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](./get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsDirty](./get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](./get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](./get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_Result](./get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](./get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](./get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](./get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](./getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](./getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_IsDirty](./set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/). |
| [set_LocaleId](./set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/). |
| [set_Result](./set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](./get_result/). |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](./update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](./update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## ملاحظات


الحقل في مستند Word هو بنية معقدة تتكون من عدة عقد تشمل بداية الحقل، شفرة الحقل، فاصل الحقل، نتيجة الحقل ونهاية الحقل. يمكن أن تكون [Fields](../) متداخلة، وتحتوي على محتوى غني وتمتد عبر فقرات أو أقسام متعددة في المستند. فئة [Field](./) هي كائن "واجهة" توفر خصائص وطرق تسمح بالعمل مع الحقل ككائن واحد.

تشير خصائص [Start](./get_start/)، [Separator](./get_separator/) و[End](./get_end/) إلى عقد بداية الحقل، الفاصل، والنهاية على التوالي.

المحتوى بين بداية الحقل والفاصل هو شفرة الحقل. المحتوى بين فاصل الحقل ونهاية الحقل هو نتيجة الحقل. عادةً ما تتكون شفرة الحقل من كائن واحد أو أكثر من [Run](../../aspose.words/run/) يحدد التعليمات. من المتوقع أن تقوم تطبيق المعالجة بتنفيذ شفرة الحقل لحساب نتيجة الحقل.

تُسمى عملية حساب نتائج الحقول بتحديث الحقل. يمكن لـ Aspose.Words تحديث نتائج الحقول لمعظم أنواع الحقول بنفس الطريقة التي يقوم بها Microsoft Word. وعلى وجه الخصوص، يمكن لـ Aspose.Words حساب نتائج حتى أكثر حقول الصيغ تعقيدًا. لحساب نتيجة حقل واحد استخدم طريقة [Update](./update/). لتحديث الحقول في المستند بالكامل استخدم [UpdateFields](../../aspose.words/document/updatefields/).

يمكنك الحصول على نسخة النص العادي من شفرة الحقل باستخدام طريقة [GetFieldCode()](./getfieldcode/). يمكنك الحصول على نسخة النص العادي من نتيجة الحقل وتعيينها باستخدام الخاصية [Result](./get_result/). يمكن لكل من شفرة الحقل ونتيجة الحقل أن تحتوي على محتوى معقد، مثل الحقول المتداخلة، الفقرات، الأشكال، الجداول، وفي هذه الحالة قد ترغب في العمل مباشرةً مع عقد الحقل إذا كنت تحتاج إلى مزيد من التحكم.

أنت لا تنشئ مثيلات من الفئة [Field](./) مباشرة. لإنشاء حقل جديد استخدم الطريقة [InsertField()](../).

## أمثلة



يظهر كيفية إدراج حقل في مستند باستخدام رمز الحقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// هذا التحميل الزائد لطريقة InsertField يقوم تلقائيًا بتحديث الحقول المدخلة.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
