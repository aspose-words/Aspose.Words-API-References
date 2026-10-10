---
title: "Aspose::Words::Document::NormalizeFieldTypes méthode"
linktitle: "NormalizeFieldTypes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::NormalizeFieldTypes méthode. Modifie les valeurs de type de champ FieldType de FieldStart, FieldSeparator, FieldEnd dans l'ensemble du document afin qu'elles correspondent aux types de champ contenus dans les codes de champ en C++."
type: docs
weight: 66000
url: /fr/cpp/aspose.words/document/normalizefieldtypes/
---
## Document::NormalizeFieldTypes method


Modifie les valeurs du type de champ [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) des [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) dans tout le document afin qu'elles correspondent aux types de champ contenus dans les codes de champ.

```cpp
void Aspose::Words::Document::NormalizeFieldTypes()
```

## Remarques


Utilisez cette méthode après des modifications du document qui affectent les types de champ.

Pour modifier les valeurs du type de champ dans une partie spécifique du document, utilisez [NormalizeFieldTypes](../../range/normalizefieldtypes/).

## Exemples



Montre comment maintenir le type d'un champ à jour avec son code de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words détecte automatiquement les types de champ en fonction des codes de champ.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// Modifiez manuellement le texte brut du champ, qui détermine le code du champ.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// La modification du code du champ a transformé ce champ en un type différent,
// mais les propriétés de type du champ affichent toujours l'ancien type.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// Mettez à jour ces propriétés avec cette méthode pour afficher la valeur actuelle.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
