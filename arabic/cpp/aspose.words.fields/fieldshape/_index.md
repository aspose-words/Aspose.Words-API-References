---
title: "فئة Aspose::Words::Fields::FieldShape"
linktitle: "FieldShape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fields::FieldShape. تنفّذ حقل SHAPE. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 93000
url: /ar/cpp/aspose.words.fields/fieldshape/
---
## FieldShape class


يُنفّذ الحقل SHAPE. لتعلم المزيد، زر [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldShape : public Aspose::Words::Fields::Field
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
| [set_Text](./set_text/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldShape::get_Text](./get_text/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

## أمثلة



يُظهر كيفية إنشاء قوائم متوافقة مع اللغات من اليمين إلى اليسار باستخدام حقول BIDIOUTLINE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حقل BIDIOUTLINE يرقم الفقرات مثل حقول AUTONUM/LISTNUM،
// ولكنه يظهر فقط عندما يتم تمكين لغة تحرير من اليمين إلى اليسار، مثل العبرية أو العربية.
// الحقل التالي سيعرض ".1"، المكافئ RTL لرقم القائمة "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// أضف حقلين إضافيين من نوع BIDIOUTLINE، سيعرضان ".2" و ".3".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// اضبط محاذاة النص الأفقية لكل فقرة في المستند إلى RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// إذا مكنّا لغة تحرير من اليمين إلى اليسار في Microsoft Word، ستعرض حقولنا أرقامًا.
// وإلا، ستعرض "###".
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


يُظهر كيف يتم التعامل مع بعض حقول Microsoft Word القديمة مثل SHAPE و EMBED أثناء التحميل.
```cpp
// افتح مستندًا تم إنشاؤه في Microsoft Word 2003.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// إذا فتحنا مستند Word وضغطنا Alt+F9، سنرى حقل SHAPE وحقل EMBED.
// حقل SHAPE هو المرفق/اللوحة لكائن AutoShape مع تمكين نمط الالتفاف "In line with text".
// حقل EMBED له نفس الوظيفة، لكنه لكائن مضمّن،
// مثل جدول بيانات من مستند Excel خارجي.
// مع ذلك، هذه الحقول لن تظهر في مجموعة الحقول الخاصة بالمستند.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// هذه الحقول مدعومة فقط في الإصدارات القديمة من Microsoft Word.
// عملية تحميل المستند ستحول هذه الحقول إلى كائنات Shape،
// والتي يمكننا الوصول إليها في مجموعة العقد الخاصة بالمستند.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// العقدة الأولى من نوع Shape تتطابق مع حقل SHAPE في المستند المدخل،
// وهي اللوحة المضمنة لكائن AutoShape.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// العقدة الثانية من نوع Shape هي AutoShape نفسها.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// العقدة الثالثة من نوع Shape هي ما كان حقل EMBED الذي يحتوي على جدول البيانات الخارجي.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
