---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: Aspose.Words för .NET
description: Utforska egenskapen HeadingPairs i BuiltInDocumentProperties för att enkelt hantera dokumentrubriker och förbättra din dokumentorganisation.
type: docs
weight: 110
url: /sv/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

Anger dokumentrubriker och deras namn.

```csharp
public object[] HeadingPairs { get; set; }
```

## Anmärkningar

Varje rubrikpar upptar två element i denna array.

Det första elementet i paret är enString och anger rubriknamnet. Det andra elementet i paret är ettInt32 och anger antalet document -delar för denna rubrik i[`TitlesOfParts`](../titlesofparts/) egendom.

Den totala summan av antal för alla rubrikpar i den här egenskapen måste vara lika med antalet element i [`TitlesOfParts`](../titlesofparts/) egendom.

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
