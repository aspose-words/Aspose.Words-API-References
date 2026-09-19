---
title: "Aspose::Words::Fields::FieldDocVariable::get_VariableName metodo"
linktitle: "get_VariableName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldDocVariable::get_VariableName metodo. Ottiene o imposta il nome della variabile del documento da recuperare in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


Ottiene o imposta il nome della variabile del documento da recuperare.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## Esempi



Mostra come utilizzare i campi DOCPROPERTY per visualizzare le proprietà del documento e le variabili.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due modi per utilizzare i campi DOCPROPERTY.
// 1 -  Visualizza una proprietà predefinita:
// Imposta un valore personalizzato per la proprietà predefinita "Category", quindi inserisci un campo DOCPROPERTY che la richiama.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Visualizza una variabile di documento personalizzata:
// Definisci una variabile personalizzata, quindi fai riferimento a quella variabile con un campo DOCPROPERTY.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## Vedi anche

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
