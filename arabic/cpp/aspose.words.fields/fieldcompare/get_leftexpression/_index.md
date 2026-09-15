---
title: "طريقة Aspose::Words::Fields::FieldCompare::get_LeftExpression"
linktitle: "get_LeftExpression"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldCompare::get_LeftExpression. يحصل أو يضبط الجزء الأيسر من تعبير المقارنة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldcompare/get_leftexpression/
---
## FieldCompare::get_LeftExpression method


يحصل أو يضبط الجزء الأيسر من تعبير المقارنة.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_LeftExpression()
```


## أمثلة



يظهر كيفية مقارنة التعبيرات باستخدام حقل COMPARE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// يعرض حقل COMPARE "0" أو "1"، اعتمادًا على صحة بيانه.
// نتيجة هذا البيان هي false لذا سيعرض هذا الحقل "0".
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// يعرض هذا الحقل "1" لأن البيان true.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## انظر أيضًا

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
