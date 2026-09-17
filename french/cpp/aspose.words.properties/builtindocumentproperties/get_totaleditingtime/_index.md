---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TotalEditingTime méthode"
linktitle: "get_TotalEditingTime"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TotalEditingTime méthode. Obtient ou définit le temps total d'édition en minutes en C++."
type: docs
weight: 31000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_totaleditingtime/
---
## BuiltInDocumentProperties::get_TotalEditingTime method


Obtient ou définit le temps total d'édition en minutes.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_TotalEditingTime()
```


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

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
