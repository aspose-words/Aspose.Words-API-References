---
title: Table.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table LeftPadding, justera enkelt avståndet mellan cellinnehåll i punkter för förbättrad layoutkontroll och förbättrad designflexibilitet.
type: docs
weight: 200
url: /sv/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

Hämtar eller anger mängden utrymme (i punkter) som ska läggas till vänster om innehållet i cellerna.

```csharp
public double LeftPadding { get; set; }
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
