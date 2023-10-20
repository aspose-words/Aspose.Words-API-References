---
title: Table.RightPadding
linktitle: RightPadding
articleTitle: RightPadding
second_title: Aspose.Words för .NET
description: Table RightPadding fast egendom. Hämtar eller ställer in mängden utrymme i poäng som ska läggas till till höger om innehållet i celler i C#.
type: docs
weight: 250
url: /sv/net/aspose.words.tables/table/rightpadding/
---
## Table.RightPadding property

Hämtar eller ställer in mängden utrymme (i poäng) som ska läggas till till höger om innehållet i celler.

```csharp
public double RightPadding { get; set; }
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

 // För varje cell i tabellen, ställ in avståndet mellan dess innehåll och var och en av dess kanter.
// Den här tabellen kommer att bibehålla det minsta utfyllnadsavståndet genom att slå in text.
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
