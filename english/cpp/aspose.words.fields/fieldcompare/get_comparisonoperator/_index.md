---
title: Aspose::Words::Fields::FieldCompare::get_ComparisonOperator method
linktitle: get_ComparisonOperator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldCompare::get_ComparisonOperator method. Gets or sets the comparison operator in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/fieldcompare/get_comparisonoperator/
---
## FieldCompare::get_ComparisonOperator method


Gets or sets the comparison operator.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_ComparisonOperator()
```


## Examples



Shows how to compare expressions using a COMPARE field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// The COMPARE field displays a "0" or a "1", depending on its statement's truth.
// The result of this statement is false so that this field will display a "0".
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// This field displays a "1" since the statement is true.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## See Also

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
