---
title: Table.DistanceLeft
linktitle: DistanceLeft
articleTitle: DistanceLeft
second_title: Aspose.Words för .NET
description: Justera egenskapen Table DistanceLeft för att kontrollera avståndet mellan tabellen och omgivande text. Förbättra läsbarhet och layout i dina dokument!
type: docs
weight: 130
url: /sv/net/aspose.words.tables/table/distanceleft/
---
## Table.DistanceLeft property

Hämtar eller ställer in avståndet mellan tabellens vänstra sida och den omgivande texten, i punkter.

```csharp
public double DistanceLeft { get; set; }
```

## Exempel

Visar hur man ställer in avståndet mellan tabellgränser och text.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

// Ange avstånd mellan tabell och omgivande text.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
