---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words för .NET
description: Aspose.Words.Tables.TableStyleOptions uppräkning. Anger hur tabellstil tillämpas på en tabell i C#.
type: docs
weight: 6370
url: /sv/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Anger hur tabellstil tillämpas på en tabell.

```csharp
[Flags]
public enum TableStyleOptions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Ingen tabellformatering tillämpas. |
| FirstRow | `20` | Använd villkorlig formatering på första raden. |
| LastRow | `40` | Använd villkorlig formatering på sista raden. |
| FirstColumn | `80` | Använd villkorlig formatering för en första kolumn. |
| LastColumn | `100` | Använd villkorlig formatering för sista kolumnen. |
| RowBands | `200` | Använd villkorlig formatering av radband. |
| ColumnBands | `400` | Använd villkorlig formatering för kolumnband. |
| Default2003 | `600` | Rad- och kolumnband tillämpas. Detta är Microsoft Word standard för gamla format som DOC, WML och RTF. |
| Default | `2A0` | Detta är Microsoft Words standardinställningar. |

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

* property [StyleOptions](../table/styleoptions/)
* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
