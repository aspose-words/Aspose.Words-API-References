---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs méthode"
linktitle: "get_HeadingPairs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs méthode. Spécifie les titres du document et leurs noms en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


Spécifie les titres du document et leurs noms.

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## Remarques


Chaque paire de titres occupe deux éléments dans ce tableau.

Le premier élément de la paire est une **String** et spécifie le nom du titre. Le deuxième élément de la paire est un **Int32** et spécifie le nombre de parties du document pour ce titre dans la propriété [TitlesOfParts](../get_titlesofparts/).

La somme totale des décomptes pour toutes les paires de titres dans cette propriété doit être égale au nombre d'éléments dans la propriété [TitlesOfParts](../get_titlesofparts/).

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
