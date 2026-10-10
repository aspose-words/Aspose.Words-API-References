---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime méthode"
linktitle: "get_LastSavedTime"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime méthode. Obtient ou définit l’heure de la dernière sauvegarde en UTC en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedtime/
---
## BuiltInDocumentProperties::get_LastSavedTime method


Obtient ou définit l'heure de la dernière sauvegarde en UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime()
```

## Remarques


Pour les documents provenant du format RTF, cette propriété renvoie l’heure locale de la dernière opération de sauvegarde.

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


Montre comment utiliser le champ SAVEDATE pour afficher la date/heure de la dernière opération d'enregistrement du document effectuée avec Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Nous pouvons utiliser le champ SAVEDATE pour afficher la date et l'heure de la dernière opération d'enregistrement sur le document.
// L'opération d'enregistrement à laquelle ces champs font référence est l'enregistrement manuel dans une application telle que Microsoft Word,
// et non la méthode Save du document.
// Ci-dessous, trois types de calendriers différents selon lesquels le champ SAVEDATE peut afficher la date/heure.
// 1 -  Calendrier lunaire islamique :
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Calendrier Umm al-Qura :
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 -  calendrier national indien :
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// Les champs SAVEDATE tirent leurs valeurs de date/heure de la propriété intégrée LastSavedTime.
// La méthode Save du document ne mettra pas à jour cette valeur, mais nous pouvons toujours la mettre à jour manuellement.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
