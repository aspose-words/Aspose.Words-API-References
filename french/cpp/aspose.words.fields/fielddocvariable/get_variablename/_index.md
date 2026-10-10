---
title: "Aspose::Words::Fields::FieldDocVariable::get_VariableName méthode"
linktitle: "get_VariableName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldDocVariable::get_VariableName méthode. Obtient ou définit le nom de la variable de document à récupérer en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


Obtient ou définit le nom de la variable de document à récupérer.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## Exemples



Montre comment utiliser les champs DOCPROPERTY pour afficher les propriétés du document et les variables.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici deux façons d'utiliser les champs DOCPROPERTY.
// 1 -  Afficher une propriété intégrée :
// Définissez une valeur personnalisée pour la propriété intégrée "Category", puis insérez un champ DOCPROPERTY qui la référence.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Afficher une variable de document personnalisée :
// Définissez une variable personnalisée, puis référencez cette variable avec un champ DOCPROPERTY.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## Voir aussi

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
