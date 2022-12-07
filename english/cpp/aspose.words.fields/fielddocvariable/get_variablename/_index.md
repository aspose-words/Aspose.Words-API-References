---
title: get_VariableName
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the document variable to retrieve.
type: docs
weight: 14
url: /cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


Gets or sets the name of the document variable to retrieve.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## Examples



Shows how to use DOCPROPERTY fields to display document properties and variables. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two ways of using DOCPROPERTY fields.
// 1 -  Display a built-in property:
// Set a custom value for the "Category" built-in property, then insert a DOCPROPERTY field that references it.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::DynamicCast<FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Display a custom document variable:
// Define a custom variable, then reference that variable with a DOCPROPERTY field.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::DynamicCast<FieldDocVariable>(builder->InsertField(FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(ArtifactsDir + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## See Also

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
