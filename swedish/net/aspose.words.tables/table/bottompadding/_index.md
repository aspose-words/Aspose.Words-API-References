---
title: Table.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table BottomPadding, justera enkelt avståndet under cellinnehållet för förbättrad layoutkontroll och förbättrad visuell tilltalning.
type: docs
weight: 90
url: /sv/net/aspose.words.tables/table/bottompadding/
---
## Table.BottomPadding property

Hämtar eller anger mängden utrymme (i punkter) som ska läggas till under innehållet i cellerna.

```csharp
public double BottomPadding { get; set; }
```

## Exempel

Visar hur man konfigurerar innehållsutfyllnad i en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // För varje cell i tabellen, ange avståndet mellan dess innehåll och var och en av dess ramar.
// Den här tabellen bibehåller det minsta utfyllnadsavståndet genom att radbryta text.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
