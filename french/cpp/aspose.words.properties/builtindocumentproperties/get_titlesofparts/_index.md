---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts méthode"
linktitle: "get_TitlesOfParts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts méthode. Chaque chaîne du tableau spécifie le nom d'une partie du document en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_titlesofparts/
---
## BuiltInDocumentProperties::get_TitlesOfParts method


Chaque chaîne du tableau spécifie le nom d'une partie du document.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts()
```

## Remarques


Aspose.Words ne met pas à jour cette propriété.

## Exemples



Affiche la relation entre les propriétés "HeadingPairs" et "TitlesOfParts".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// Nous pouvons trouver les valeurs combinées de ces collections via
// "Fichier" -> "Propriétés" -> "Propriétés avancées" -> "Onglet Contenus".
// La propriété HeadingPairs est une collection de paires <string, int> qui
// détermine combien de parties du document un titre couvre.
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// La propriété TitlesOfParts contient les noms des parties qui appartiennent aux titres ci-dessus.
System::ArrayPtr<System::String> titlesOfParts = doc->get_BuiltInDocumentProperties()->get_TitlesOfParts();

int32_t headingPairsIndex = 0;
int32_t titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs->get_Length())
{
    std::cout << System::String::Format(u"Parts for {0}:", headingPairs[headingPairsIndex++]) << std::endl;
    int32_t partsCount = System::Convert::ToInt32(headingPairs[headingPairsIndex++]);

    for (int32_t i = 0; i < partsCount; i++)
    {
        std::cout << System::String::Format(u"\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]) << std::endl;
    }
}
```

## Voir aussi

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
