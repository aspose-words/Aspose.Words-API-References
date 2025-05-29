---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TitlesOfParts i BuiltInDocumentProperties. Hantera enkelt dokumentavsnitt med tydliga, anpassningsbara delnamn för förbättrad organisation.
type: docs
weight: 330
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

Visar förhållandet mellan egenskaperna "HeadingPairs" och "TitlesOfParts".

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// Vi kan hitta de kombinerade värdena för dessa samlingar via
// "Arkiv" -> "Egenskaper" -> "Avancerade egenskaper" -> fliken "Innehåll".
// Egenskapen HeadingPairs är en samling av <string, int> par som
// avgör hur många dokumentdelar en rubrik sträcker sig över.
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// Egenskapen TitlesOfParts innehåller namnen på de delar som hör till rubrikerna ovan.
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
