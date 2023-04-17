---
title: Aspose::Words::Fields::FieldIf::get_RightExpression method
linktitle: get_RightExpression
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldIf::get_RightExpression method. Gets or sets the right part of the comparison expression in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.fields/fieldif/get_rightexpression/
---
## FieldIf::get_RightExpression method


Gets or sets the right part of the comparison expression.

```cpp
System::String Aspose::Words::Fields::FieldIf::get_RightExpression()
```


## Examples



Shows how to insert an IF field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::DynamicCast<FieldIf>(builder->InsertField(FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// The IF field will display a string from either its "TrueText" property,
// or its "FalseText" property, depending on the truth of the statement that we have constructed.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// In this case, "0 = 1" is incorrect, so the displayed result will be "False".
ASSERT_EQ(u" IF  0 = 1 True False", field->GetFieldCode());
ASSERT_EQ(FieldIfComparisonResult::False, field->EvaluateCondition());
ASSERT_EQ(u"False", field->get_Result());

builder->Write(u"\nStatement 2: ");
field = System::DynamicCast<FieldIf>(builder->InsertField(FieldType::FieldIf, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// This time the statement is correct, so the displayed result will be "True".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.IF.docx");
```

## See Also

* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
