---
title: Table.AutoFit
linktitle: AutoFit
articleTitle: AutoFit
second_title: Aspose.Words för .NET
description: Upptäck metoden för automatisk anpassning av tabeller för att enkelt ändra storlek på tabeller och celler för optimal layout. Förbättra presentationen av ditt dokument med lätthet!
type: docs
weight: 380
url: /sv/net/aspose.words.tables/table/autofit/
---
## Table.AutoFit method

Ändrar storleken på tabellen och cellerna enligt det angivna automatiska anpassningsbeteendet.

```csharp
public void AutoFit(AutoFitBehavior behavior)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| behavior | AutoFitBehavior | Anger hur tabellen ska anpassas automatiskt. |

## Anmärkningar

Den här metoden härmar kommandona som finns i menyn Anpassa automatiskt för en tabell i Microsoft Word. De tillgängliga kommandona är "Anpassa automatiskt till innehåll", "Anpassa automatiskt till fönster" och "Fast kolumnbredd". I Microsoft Word ställer dessa kommandon in relevanta tabellegenskaper och uppdaterar sedan tabelllayouten, så gör Aspose.Words detsamma åt dig.

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

* enum [AutoFitBehavior](../../autofitbehavior/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
