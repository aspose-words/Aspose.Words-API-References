---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TitlesOfParts dans BuiltInDocumentProperties. Gérez facilement les sections de vos documents grâce à des noms de parties clairs et personnalisables pour une organisation optimisée.
type: docs
weight: 330
url: /fr/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Chaque chaîne du tableau spécifie le nom d'une partie du document.

```csharp
public string[] TitlesOfParts { get; set; }
```

## Remarques

Aspose.Words ne met pas à jour cette propriété.

## Exemples

Affiche la relation entre les propriétés « HeadingPairs » et « TitlesOfParts ».

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Nous pouvons trouver les valeurs combinées de ces collections via
// "Fichier" -> "Propriétés" -> "Propriétés avancées" -> onglet "Contenu".
// La propriété HeadingPairs est une collection de paires <string, int> qui
// détermine le nombre de parties du document sur lesquelles s'étend un titre.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// La propriété TitlesOfParts contient les noms des parties qui appartiennent aux en-têtes ci-dessus.
string[] titlesOfParts = doc.BuiltInDocumentProperties.TitlesOfParts;

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs.Length)
{
    Console.WriteLine($"Parts for {headingPairs[headingPairsIndex++]}:");
    int partsCount = Convert.ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
        Console.WriteLine($"\t\"{titlesOfParts[titlesOfPartsIndex++]}\"");
}
```

### Voir également

* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
