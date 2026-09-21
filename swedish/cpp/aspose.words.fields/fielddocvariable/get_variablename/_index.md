---
title: "Aspose::Words::Fields::FieldDocVariable::get_VariableName‑metod"
linktitle: "get_VariableName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldDocVariable::get_VariableName‑metod. Hämtar eller anger namnet på dokumentvariabeln som ska hämtas i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


Hämtar eller anger namnet på dokumentvariabeln som ska hämtas.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## Exempel



Visar hur man använder DOCPROPERTY‑fält för att visa dokumentegenskaper och variabler.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan följer två sätt att använda DOCPROPERTY‑fält.
// 1 -  Visa en inbyggd egenskap:
// Ange ett anpassat värde för den inbyggda egenskapen "Category", och infoga sedan ett DOCPROPERTY‑fält som refererar till den.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Visa en anpassad dokumentvariabel:
// Definiera en anpassad variabel, och referera sedan till den variabeln med ett DOCPROPERTY‑fält.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## Se även

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
