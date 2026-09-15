---
title: "Aspose::Words::Fields::FieldListNum::get_HasListName طريقة"
linktitle: "get_HasListName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldListNum::get_HasListName طريقة. تُعيد قيمة تشير إلى ما إذا كان اسم تعريف الترقيم التجريدي مُقدَّمًا بواسطة شفرة الحقل في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldlistnum/get_haslistname/
---
## FieldListNum::get_HasListName method


يرجع قيمة تشير إلى ما إذا كان اسم تعريف الترقيم المجرد مُقدَّمًا بواسطة شفرة الحقل.

```cpp
bool Aspose::Words::Fields::FieldListNum::get_HasListName()
```


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

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
