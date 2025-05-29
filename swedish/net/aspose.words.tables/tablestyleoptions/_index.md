---
title: TableStyleOptions Enum
linktitle: TableStyleOptions
articleTitle: TableStyleOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Tables.TableStyleOptions-enumet för flexibel tabellformatering. Förbättra din dokumentdesign med anpassningsbara tabellformat idag!
type: docs
weight: 7220
url: /sv/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Anger hur tabellformatet tillämpas på en tabell.

```csharp
[Flags]
public enum TableStyleOptions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Ingen tabellformatering tillämpas. |
| FirstRow | `20` | Använd villkorsstyrd formatering på första raden. |
| LastRow | `40` | Använd villkorsstyrd formatering för sista raden. |
| FirstColumn | `80` | Använd villkorsstyrd formatering för 1 första kolumn. |
| LastColumn | `100` | Använd villkorsstyrd formatering för sista kolumnen. |
| RowBands | `200` | Använd villkorsstyrd formatering för radband. |
| ColumnBands | `400` | Använd villkorsstyrd formatering för kolumnränder. |
| Default2003 | `600` | Rad- och kolumnbandering tillämpas. Detta är standard i Microsoft Word för gamla format som DOC, WML och RTF. |
| Default | `2A0` | Detta är standardinställningarna för Microsoft Word. |

## Exempel

Visar hur man skapar en ny tabell samtidigt som man tillämpar en stil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Vi måste infoga minst en rad innan vi anger någon tabellformatering.
builder.InsertCell();

// Ange tabellstilen som används baserat på stilidentifieraren.
// Observera att inte alla tabellformat är tillgängliga när man sparar i .doc-format.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Tillämpa delvis stilen på tabellens funktioner baserat på predikat, och bygg sedan tabellen.
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
