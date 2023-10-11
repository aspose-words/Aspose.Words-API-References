---
title: Table.DistanceTop
second_title: Aspose.Words för .NET API Referens
description: Table fast egendom. Hämtar eller ställer in avståndet mellan bordsskivan och den omgivande texten i punkter.
type: docs
weight: 150
url: /sv/net/aspose.words.tables/table/distancetop/
---
## Table.DistanceTop property

Hämtar eller ställer in avståndet mellan bordsskivan och den omgivande texten, i punkter.

```csharp
public double DistanceTop { get; set; }
```

### Exempel

Visar hur man ställer in avståndet mellan tabellgränser och text.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

 // Ställ in avståndet mellan tabell och omgivande text.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../table/)
* hopsättning [Aspose.Words](../../../)


