---
title: Aspose::Words::Fields::FieldCompare::get_LeftExpression method
linktitle: get_LeftExpression
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldCompare::get_LeftExpression method. Gets or sets the left part of the comparison expression in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fields/fieldcompare/get_leftexpression/
---
## FieldCompare::get_LeftExpression method


Gets or sets the left part of the comparison expression.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_LeftExpression()
```


## Examples



Shows how to compare expressions using a COMPARE field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto field = System::DynamicCast<FieldCompare>(builder->InsertField(FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// The COMPARE field displays a "0" or a "1", depending on its statement's truth.
// The result of this statement is false so that this field will display a "0".
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::DynamicCast<FieldCompare>(builder->InsertField(FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// This field displays a "1" since the statement is true.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.COMPARE.docx");
```

## See Also

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
