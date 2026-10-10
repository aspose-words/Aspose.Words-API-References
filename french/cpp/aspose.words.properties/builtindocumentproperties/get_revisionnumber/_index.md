---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber méthode"
linktitle: "get_RevisionNumber"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber méthode. Obtient ou définit le numéro de révision du document en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_revisionnumber/
---
## BuiltInDocumentProperties::get_RevisionNumber method


Obtient ou définit le numéro de révision du document.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber()
```

## Remarques


Aspose.Words ne met pas à jour cette propriété.

## Exemples



Montre comment travailler avec les propriétés du document dans la catégorie "Origin".
```cpp
// Ouvrez un document que nous avons créé et modifié à l'aide de Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Les propriétés intégrées suivantes contiennent des informations concernant la création et la modification de ce document.
// Nous pouvons cliquer avec le bouton droit sur ce document dans l'Explorateur Windows et trouver
// ces propriétés via "Propriétés" -> "Détails" -> catégorie "Origin".
// Des champs tels que PRINTDATE et EDITTIME peuvent afficher ces valeurs dans le corps du document.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// Nous pouvons également modifier les valeurs des propriétés intégrées.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word met à jour les propriétés suivantes automatiquement lorsque nous enregistrons le document.
// Pour utiliser ces propriétés avec Aspose.Words, nous devrons définir leurs valeurs manuellement.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// Nous pouvons cliquer avec le bouton droit sur ce document dans l'Explorateur Windows et trouver ces propriétés dans "Propriétés" -> "Détails" -> "Origin".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```


Montre comment travailler avec les champs REVNUM.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Current revision #");

// Insérez un champ REVNUM, qui affiche la propriété du numéro de révision actuel du document.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRevNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRevisionNum, true));

ASSERT_EQ(u" REVNUM ", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_RevisionNumber());

// Cette propriété compte le nombre de fois qu'un document a été enregistré dans Microsoft Word,
// et n'est pas liée aux révisions suivies. Nous pouvons la trouver en cliquant avec le bouton droit sur le document dans l'Explorateur Windows
// via Propriétés -> Détails. Nous pouvons mettre à jour cette propriété manuellement.
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LVAL_LAMBDA_ARGS(doc->get_BuiltInDocumentProperties(), RevisionNumber));
field->Update();

ASSERT_EQ(u"2", field->get_Result());
```

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
