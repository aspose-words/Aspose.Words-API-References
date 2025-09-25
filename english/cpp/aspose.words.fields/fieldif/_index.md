---
title: Aspose::Words::Fields::FieldIf class
linktitle: FieldIf
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldIf class. Implements the IF field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 54000
url: /cpp/aspose.words.fields/fieldif/
---
## FieldIf class


Implements the IF field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldIf : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Methods

| Method | Description |
| --- | --- |
| [EvaluateCondition](./evaluatecondition/)() | Evaluates the condition. |
| [get_ComparisonOperator](./get_comparisonoperator/)() | Gets or sets the comparison operator. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](./get_end/)() override | Gets the node that represents the field end. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FalseText](./get_falsetext/)() | Gets or sets the text displayed if the comparison expression is **false**. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LeftExpression](./get_leftexpression/)() | Gets or sets the left part of the comparison expression. |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_RightExpression](./get_rightexpression/)() | Gets or sets the right part of the comparison expression. |
| [get_Separator](./get_separator/)() override | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](./get_start/)() override | Gets the node that represents the start of the field. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_TrueText](./get_truetext/)() | Gets or sets the text displayed if the comparison expression is true. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_ComparisonOperator](./set_comparisonoperator/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIf::get_ComparisonOperator](./get_comparisonoperator/). |
| [set_FalseText](./set_falsetext/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIf::get_FalseText](./get_falsetext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftExpression](./set_leftexpression/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIf::get_LeftExpression](./get_leftexpression/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightExpression](./set_rightexpression/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIf::get_RightExpression](./get_rightexpression/). |
| [set_TrueText](./set_truetext/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIf::get_TrueText](./get_truetext/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## Remarks


Compares the values designated by the expressions [LeftExpression](./get_leftexpression/) and [RightExpression](./get_rightexpression/) in comparison using the operator designated by [ComparisonOperator](./get_comparisonoperator/).

A field in the following format will be used as a mail merge source: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

## Examples



Shows how to insert an IF field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
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

// This time the statement is correct, so the displayed result will be "True".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
