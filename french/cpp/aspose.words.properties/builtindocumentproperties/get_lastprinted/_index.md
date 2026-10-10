---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted méthode"
linktitle: "get_LastPrinted"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted méthode. Obtient ou définit la date à laquelle le document a été imprimé pour la dernière fois en UTC en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_lastprinted/
---
## BuiltInDocumentProperties::get_LastPrinted method


Obtient ou définit la date à laquelle le document a été imprimé pour la dernière fois en UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted()
```

## Remarques


Pour les documents issus du format RTF, cette propriété renvoie l'heure locale de la dernière impression.

Si le document n'a jamais été imprimé, cette propriété renverra DateTime.MinValue.

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

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
