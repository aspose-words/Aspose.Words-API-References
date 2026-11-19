---
title: Aspose::Words::Fields::FieldDocVariable::set_VariableName method
linktitle: set_VariableName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldDocVariable::set_VariableName method. Sets the name of the document variable to retrieve in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fields/fielddocvariable/set_variablename/
---
## FieldDocVariable::set_VariableName method


Sets the name of the document variable to retrieve.

```cpp
void Aspose::Words::Fields::FieldDocVariable::set_VariableName(const System::String & value)
```

## Examples


Shows how to use DOCPROPERTY fields to display document properties and variables.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are two ways of using DOCPROPERTY fields.
// 1 -  Display a built-in property:
// Set a custom value for the "Category" built-in property, then insert a DOCPROPERTY field that references it.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(fieldDocProperty->GetFieldCode(), u" DOCPROPERTY Category ");
ASSERT_EQ(fieldDocProperty->get_Result(), u"My category");

builder->InsertParagraph();

// 2 -  Display a custom document variable:
// Define a custom variable, then reference that variable with a DOCPROPERTY field.
ASSERT_EQ(doc->get_Variables()->get_Count(), 0);
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(fieldDocVariable->GetFieldCode(), u" DOCVARIABLE  \"My Variable\"");
ASSERT_EQ(fieldDocVariable->get_Result(), u"My variable's value");

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```
## See Also

* [get_VariableName](../get_variablename/)

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
