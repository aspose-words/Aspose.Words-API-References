---
title: "Aspose::Words::Fields::FieldListNum class"
linktitle: "FieldListNum"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldListNum class. ينفّذ حقل LISTNUM. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 64000
url: /ar/cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


ينفذ حقل LISTNUM. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_HasListName](./get_haslistname/)() | يرجع قيمة تشير إلى ما إذا كان اسم تعريف الترقيم المجرد مُقدَّمًا بواسطة شفرة الحقل. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_ListLevel](./get_listlevel/)() | يحصل أو يعيّن المستوى في القائمة، متجاوزًا السلوك الافتراضي للحقل. |
| [get_ListName](./get_listname/)() | يحصل أو يعيّن اسم تعريف الترقيم المجرد المستخدم للترقيم. |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_StartingNumber](./get_startingnumber/)() | يحصل أو يضبط القيمة الأولية لهذا الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() override | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/). |
| [set_ListName](./set_listname/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

## أمثلة



يظهر كيفية ترقيم الفقرات باستخدام حقول LISTNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حقول LISTNUM تعرض رقمًا يزداد في كل حقل LISTNUM.
// تحتوي هذه الحقول أيضًا على مجموعة متنوعة من الخيارات التي تتيح لنا استخدامها لمحاكاة القوائم المرقمة.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// تبدأ القوائم العد من 1 بشكل افتراضي، لكن يمكننا ضبط هذا الرقم إلى قيمة مختلفة، مثل 0.
// سيعرض هذا الحقل "0)".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// تحافظ حقول LISTNUM على عدّات منفصلة لكل مستوى قائمة.
// إدراج حقل LISTNUM في نفس الفقرة مع حقل LISTNUM آخر
// يزيد مستوى القائمة بدلاً من العد.
// الحقل التالي سيستمر في العد الذي بدأناه أعلاه ويعرض قيمة "1" في المستوى 1.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// سيبدأ هذا الحقل عدًا في المستوى 2. سيعرض قيمة "1".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// سيبدأ هذا الحقل عدًا في المستوى 3. سيعرض قيمة "1".
// المستويات المختلفة للقائمة لها تنسيقات مختلفة،
// لذلك ستعرض هذه الحقول مجتمعة قيمة "1)a)i)".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// الحقل LISTNUM التالي الذي نقوم بإدراجه سيستمر في العد عند مستوى القائمة
// الذي كان عليه الحقل LISTNUM السابق.
// يمكننا استخدام الخاصية "ListLevel" للانتقال إلى مستوى قائمة مختلف.
// إذا ظل هذا الحقل LISTNUM في المستوى 3، فسيعرض "ii)",
// ولكن، بما أننا نقلناه إلى المستوى 2، فإنه يواصل العد في ذلك المستوى ويعرض "b)".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// يمكننا ضبط الخاصية ListName لجعل الحقل يحاكي نوع حقل AUTONUM مختلف.
// "NumberDefault" يحاكي AUTONUM، "OutlineDefault" يحاكي AUTONUMOUT،
// و "LegalDefault" يحاكي حقول AUTONUMLGL.
// الاسم "OutlineDefault" للقائمة مع 1 كرقم بدء سيؤدي إلى عرض "I.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// الـ ListName لا ينتقل من الحقل السابق، لذلك سنحتاج إلى تعيينه لكل حقل جديد.
// هذا الحقل يواصل العد باستخدام اسم قائمة مختلف ويعرض "II.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
