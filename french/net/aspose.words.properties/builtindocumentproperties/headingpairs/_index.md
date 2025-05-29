---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: Aspose.Words pour .NET
description: Explorez la propriété HeadingPairs dans BuiltInDocumentProperties pour gérer facilement les en-têtes de documents et améliorer l'organisation de vos documents.
type: docs
weight: 110
url: /fr/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Spécifie les en-têtes de document et leurs noms.

```csharp
public object[] HeadingPairs { get; set; }
```

## Remarques

Chaque paire d'en-têtes occupe deux éléments dans ce tableau.

Le premier élément de la paire est unString et spécifie le nom du titre. Le deuxième élément de la paire est unInt32 et spécifie le nombre de pièces document pour cette rubrique dans le[`TitlesOfParts`](../titlesofparts/) propriété.

La somme totale des comptes pour toutes les paires d'en-têtes dans cette propriété doit être égale au nombre d'éléments dans le[`TitlesOfParts`](../titlesofparts/) propriété.

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
