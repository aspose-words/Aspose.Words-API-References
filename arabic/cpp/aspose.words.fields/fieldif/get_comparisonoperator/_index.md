---
title: "طريقة Aspose::Words::Fields::FieldIf::get_ComparisonOperator"
linktitle: "get_ComparisonOperator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldIf::get_ComparisonOperator. يحصل على أو يضبط عامل المقارنة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldif/get_comparisonoperator/
---
## FieldIf::get_ComparisonOperator method


يحصل أو يضبط عامل المقارنة.

```cpp
System::String Aspose::Words::Fields::FieldIf::get_ComparisonOperator()
```


## أمثلة



يعرض كيفية إدراج حقل IF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// سيعرض حقل IF سلسلة إما من خاصية "TrueText" الخاصة به،
// أو من خاصية "FalseText" الخاصة به، اعتمادًا على صحة العبارة التي أنشأناها.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// في هذه الحالة، "0 = 1" غير صحيحة، لذا ستكون النتيجة المعروضة "False".
ASSERT_EQ(u" IF  0 = 1 True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::False, field->EvaluateCondition());
ASSERT_EQ(u"False", field->get_Result());

builder->Write(u"\nStatement 2: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// هذه المرة العبارة صحيحة، لذا ستكون النتيجة المعروضة "True".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## انظر أيضًا

* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
