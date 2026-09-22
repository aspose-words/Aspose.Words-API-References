---
title: "فئة Aspose::Words::Fields::FieldQuote"
linktitle: "FieldQuote"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldQuote. تنفذ حقل QUOTE. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 83000
url: /ar/cpp/aspose.words.fields/fieldquote/
---
## FieldQuote class


يُنفّذ الحقل QUOTE. لتعلم المزيد، زر [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldQuote : public Aspose::Words::Fields::Field
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
| [get_Text](./get_text/)() | يحصل أو يضبط النص المراد استرجاعه. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_Text](./set_text/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Fields::FieldQuote::get_Text](./get_text/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

## أمثلة



يُظهر كيفية استخدام حقل QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج حقل QUOTE، الذي سيعرض قيمة خاصية Text الخاصة به.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// أدرج حقل QUOTE وضمّن داخله حقل DATE.
// تُحدّث حقول DATE قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
// إدراج حقل DATE داخل حقل QUOTE بهذه الطريقة سيجمد قيمته
// إلى التاريخ الذي أنشأنا فيه المستند.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// حدّث جميع الحقول لعرض نتائجها الصحيحة.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
