---
title: "طريقة Aspose::Words::Fields::FieldIf::EvaluateCondition"
linktitle: "EvaluateCondition"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldIf::EvaluateCondition. يقيم الشرط في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldif/evaluatecondition/
---
## FieldIf::EvaluateCondition method


يقيم الشرط.

```cpp
Aspose::Words::Fields::FieldIfComparisonResult Aspose::Words::Fields::FieldIf::EvaluateCondition()
```


### ReturnValue

قيمة [FieldIfComparisonResult](../../fieldifcomparisonresult/) تمثل نتيجة تقييم الشرط.

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

* Enum [FieldIfComparisonResult](../../fieldifcomparisonresult/)
* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
