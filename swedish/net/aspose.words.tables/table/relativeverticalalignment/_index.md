---
title: Table.RelativeVerticalAlignment
linktitle: RelativeVerticalAlignment
articleTitle: RelativeVerticalAlignment
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table RelativeVerticalAlignment för att enkelt hantera vertikal justering för flytande tabeller, vilket förbättrar din layouts precision och design.
type: docs
weight: 240
url: /sv/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

Hämtar eller ställer in den flytande tabellens relativa vertikala justering.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
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

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
