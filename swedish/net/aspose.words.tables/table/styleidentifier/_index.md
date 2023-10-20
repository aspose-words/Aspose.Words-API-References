---
title: Table.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words för .NET
description: Table StyleIdentifier fast egendom. Hämtar eller ställer in den språkoberoende stilidentifieraren för tabellstilen som tillämpas på denna tabell i C#.
type: docs
weight: 280
url: /sv/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

Hämtar eller ställer in den språkoberoende stilidentifieraren för tabellstilen som tillämpas på denna tabell.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Exempel

Visar hur man bygger en ny tabell samtidigt som man använder en stil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Vi måste infoga minst en rad innan vi ställer in någon tabellformatering.
builder.InsertCell();

// Ställ in tabellstilen som används baserat på stilidentifieraren.
// Observera att inte alla tabellstilar är tillgängliga när du sparar i .doc-format.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Tillämpa stilen delvis på funktioner i tabellen baserat på predikat, bygg sedan tabellen.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Se även

* enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
