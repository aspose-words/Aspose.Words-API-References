---
title: "فئة Aspose::Words::Fields::FieldDate"
linktitle: "FieldDate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldDate. تنفّذ حقل DATE. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words.fields/fielddate/
---
## FieldDate class


يُنفّذ حقل DATE. لمزيد من المعلومات، زر [العمل مع الحقول](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldDate : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                  public Aspose::Words::Fields::IFieldWithCalendar
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [get_UseLastFormat](./get_uselastformat/)() | يحصل أو يعيّن ما إذا كان سيُستخدم التنسيق الذي استخدمته آخر مرة من قبل التطبيق المستضيف عند إدراج حقل DATE جديد. |
| [get_UseLunarCalendar](./get_uselunarcalendar/)() override | يحصل أو يضبط ما إذا كان سيتم استخدام التقويم القمري الهجري أو التقويم القمري العبري. |
| [get_UseSakaEraCalendar](./get_usesakaeracalendar/)() override | يحصل أو يضبط ما إذا كان سيتم استخدام تقويم عهد سكا. |
| [get_UseUmAlQuraCalendar](./get_useumalquracalendar/)() override | يحصل أو يضبط ما إذا كان سيتم استخدام تقويم أم القرى. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_UseLastFormat](./set_uselastformat/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldDate::get_UseLastFormat](./get_uselastformat/). |
| [set_UseLunarCalendar](./set_uselunarcalendar/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldDate::get_UseLunarCalendar](./get_uselunarcalendar/). |
| [set_UseSakaEraCalendar](./set_usesakaeracalendar/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldDate::get_UseSakaEraCalendar](./get_usesakaeracalendar/). |
| [set_UseUmAlQuraCalendar](./set_useumalquracalendar/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar](./get_useumalquracalendar/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

## أمثلة



يظهر كيفية استخدام حقول DATE لعرض التواريخ وفقًا لأنواع مختلفة من التقويمات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إذا أردنا أن يعرض النص في المستند دائمًا التاريخ الصحيح، يمكننا استخدام حقل DATE.
// فيما يلي ثلاثة أنواع من التقويمات الثقافية التي يمكن لحقل DATE استخدامها لعرض تاريخ.
// 1 -  التقويم القمري الإسلامي:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  تقويم أم القرى:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  التقويم الوطني الهندي:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// أدرج حقل DATE وحدد نوع تقويمه إلى النوع الذي استخدمه التطبيق المستضيف آخر مرة.
// في Microsoft Word، سيكون النوع هو الأكثر استخدامًا مؤخرًا في مربع الحوار إدراج -> نص -> تاريخ ووقت.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
