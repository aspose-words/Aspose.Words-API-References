---
title: Table.AbsoluteHorizontalDistance
linktitle: AbsoluteHorizontalDistance
articleTitle: AbsoluteHorizontalDistance
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table AbsoluteHorizontalDistance för att enkelt justera din tabells horisontella position i punkter. Optimera layouten med standardvärdet 0!
type: docs
weight: 20
url: /sv/net/aspose.words.tables/table/absolutehorizontaldistance/
---
## Table.AbsoluteHorizontalDistance property

Hämtar eller ställer in absolut horisontell flytande tabellposition som anges av tabellegenskaperna, i punkter. Standardvärdet är 0.

```csharp
public double AbsoluteHorizontalDistance { get; set; }
```

## Exempel

Visar hur man ställer in placeringen av flytande tabeller.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Ange tabellens plats på sidan, till exempel i det här fallet det nedre högra hörnet.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Vi kan också ange en horisontell och vertikal förskjutning i punkter från styckets plats där vi infogade tabellen.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
