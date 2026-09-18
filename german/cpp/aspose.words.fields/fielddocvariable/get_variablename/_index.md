---
title: "Aspose::Words::Fields::FieldDocVariable::get_VariableName Methode"
linktitle: "get_VariableName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldDocVariable::get_VariableName Methode. Gibt den Namen der Dokumentvariablen zurück oder legt ihn fest, um ihn in C++ abzurufen."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


Liest oder setzt den Namen der abzurufenden Dokumentvariablen.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## Beispiele



Zeigt, wie DOCPROPERTY-Felder verwendet werden, um Dokumenteigenschaften und Variablen anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Im Folgenden werden zwei Methoden zur Verwendung von DOCPROPERTY-Feldern gezeigt.
// 1 -  Eine integrierte Eigenschaft anzeigen:
// Legen Sie einen benutzerdefinierten Wert für die integrierte Eigenschaft \"Category\" fest und fügen Sie anschließend ein DOCPROPERTY-Feld ein, das darauf verweist.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Eine benutzerdefinierte Dokumentvariable anzeigen:
// Definieren Sie eine benutzerdefinierte Variable und verweisen Sie dann mit einem DOCPROPERTY-Feld auf diese Variable.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## Siehe auch

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
