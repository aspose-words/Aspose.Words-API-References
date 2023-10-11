---
title: BuiltInDocumentProperties.HeadingPairs
second_title: Référence de l'API Aspose.Words pour .NET
description: BuiltInDocumentProperties propriété. Spécifie les entêtes des documents et leurs noms.
type: docs
weight: 110
url: /fr/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Spécifie les en-têtes des documents et leurs noms.

```csharp
public object[] HeadingPairs { get; set; }
```

### Remarques

Chaque paire de titres occupe deux éléments de ce tableau.

Le premier élément de la paire est unString et précise le nom de la rubrique. Le deuxième élément de la paire est unInt32 et spécifie le nombre de parties document pour cet en-tête dans le[`TitlesOfParts`](../titlesofparts/) propriété.

La somme totale des comptes pour toutes les paires de titres de cette propriété doit être égale au nombre d'éléments dans la propriété.[`TitlesOfParts`](../titlesofparts/) propriété.

Aspose.Words ne met pas à jour cette propriété.

### Exemples

Affiche la relation entre les propriétés « HeadingPairs » et « TitlesOfParts ».

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// On peut trouver les valeurs combinées de ces collections via
// "Fichier" -> "Propriétés" -> "Propriétés avancées" -> Onglet "Contenu".
// La propriété HeadingPairs est une collection de <string, int> des paires qui
// détermine le nombre de parties de document qu'un en-tête couvre.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// La propriété TitlesOfParts contient les noms des parties appartenant aux en-têtes ci-dessus.
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
* espace de noms [Aspose.Words.Properties](../../builtindocumentproperties/)
* Assemblée [Aspose.Words](../../../)


