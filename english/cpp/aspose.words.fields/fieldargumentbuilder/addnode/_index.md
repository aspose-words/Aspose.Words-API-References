---
title: Aspose::Words::Fields::FieldArgumentBuilder::AddNode method
linktitle: AddNode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldArgumentBuilder::AddNode method. Adds a node to the argument in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fields/fieldargumentbuilder/addnode/
---
## FieldArgumentBuilder::AddNode method


Adds a node to the argument.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldArgumentBuilder> Aspose::Words::Fields::FieldArgumentBuilder::AddNode(const System::SharedPtr<Aspose::Words::Inline> &node)
```


## Examples



Shows how to construct fields using a field builder, and then insert them into the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Below are three examples of field construction done using a field builder.
// 1 -  Single field:
// Use a field builder to add a SYMBOL field which displays the ƒ (Florin) symbol.
auto builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(402);
builder->AddSwitch(u"\\f", u"Arial");
builder->AddSwitch(u"\\s", 25);
builder->AddSwitch(u"\\u");
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph());

ASSERT_EQ(u" SYMBOL 402 \\f Arial \\s 25 \\u ", field->GetFieldCode());

// 2 -  Nested field:
// Use a field builder to create a formula field used as an inner field by another field builder.
auto innerFormulaBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
innerFormulaBuilder->AddArgument(100);
innerFormulaBuilder->AddArgument(u"+");
innerFormulaBuilder->AddArgument(74);

// Create another builder for another SYMBOL field, and insert the formula field
// that we have created above into the SYMBOL field as its argument.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldSymbol);
builder->AddArgument(innerFormulaBuilder);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

// The outer SYMBOL field will use the formula field result, 174, as its argument,
// which will make the field display the ® (Registered Sign) symbol since its character number is 174.
ASSERT_EQ(u" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field->GetFieldCode());

// 3 -  Multiple nested fields and arguments:
// Now, we will use a builder to create an IF field, which displays one of two custom string values,
// depending on the true/false value of its expression. To get a true/false value
// that determines which string the IF field displays, the IF field will test two numeric expressions for equality.
// We will provide the two expressions in the form of formula fields, which we will nest inside the IF field.
auto leftExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
leftExpression->AddArgument(2);
leftExpression->AddArgument(u"+");
leftExpression->AddArgument(3);

auto rightExpression = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldFormula);
rightExpression->AddArgument(2.5);
rightExpression->AddArgument(u"*");
rightExpression->AddArgument(5.2);

// Next, we will build two field arguments, which will serve as the true/false output strings for the IF field.
// These arguments will reuse the output values of our numeric expressions.
auto trueOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
trueOutput->AddText(u"True, both expressions amount to ");
trueOutput->AddField(leftExpression);

auto falseOutput = System::MakeObject<Aspose::Words::Fields::FieldArgumentBuilder>();
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u"False, "));
falseOutput->AddField(leftExpression);
falseOutput->AddNode(System::MakeObject<Aspose::Words::Run>(doc, u" does not equal "));
falseOutput->AddField(rightExpression);

// Finally, we will create one more field builder for the IF field and combine all of the expressions.
builder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldIf);
builder->AddArgument(leftExpression);
builder->AddArgument(u"=");
builder->AddArgument(rightExpression);
builder->AddArgument(trueOutput);
builder->AddArgument(falseOutput);
field = builder->BuildAndInsert(doc->get_FirstSection()->get_Body()->AppendParagraph(System::String::Empty));

ASSERT_EQ(System::String(u" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 ") + u"\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " + u"\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## See Also

* Class [FieldArgumentBuilder](../)
* Class [Inline](../../../aspose.words/inline/)
* Class [FieldArgumentBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
