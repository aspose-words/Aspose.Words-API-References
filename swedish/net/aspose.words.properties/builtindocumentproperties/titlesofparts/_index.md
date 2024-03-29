---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words för .NET
description: BuiltInDocumentProperties TitlesOfParts fast egendom. Varje sträng i arrayen anger namnet på en del i dokumentet i C#.
type: docs
weight: 300
url: /sv/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

Varje sträng i arrayen anger namnet på en del i dokumentet.

```csharp
public string[] TitlesOfParts { get; set; }
```

## Anmärkningar

Aspose.Words uppdaterar inte den här egenskapen.

## Exempel

Visar förhållandet mellan "HeadingPairs" och "TitlesOfParts" egenskaper.

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Vi kan hitta de kombinerade värdena för dessa samlingar via
// "Fil" -> "Egenskaper" -> "Avancerade egenskaper" -> Fliken "Innehåll".
// Egenskapen HeadingPairs är en samling av <string, int> parar det
// bestämmer hur många dokumentdelar en rubrik sträcker sig över.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// Egenskapen TitlesOfParts innehåller namnen på delar som hör till ovanstående rubriker.
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

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
