---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words för .NET
description: Aspose.Words.Tables.PreferredWidth klass. Representerar ett värde och dess måttenhet som används för att ange den föredragna bredden på en tabell eller en cell i C#.
type: docs
weight: 6290
url: /sv/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Representerar ett värde och dess måttenhet som används för att ange den föredragna bredden på en tabell eller en cell.

För att lära dig mer, besök[Arbeta med tabeller](https://docs.aspose.com/words/net/working-with-tables/) dokumentationsartikel.

```csharp
public sealed class PreferredWidth
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Hämtar måttenheten som används för detta föredragna breddvärde. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Hämtar önskat breddvärde. Måttenheten anges i[`Type`](./type/) egenskap. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | En skapandemetod som returnerar en ny instans som representerar en föredragen bredd som anges i procent. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | En skapandemetod som returnerar en ny instans som representerar en föredragen bredd som anges med ett antal punkter. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | Bestämmer om det angivna objektet har samma värde som det aktuella objektet. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | Bestämmer om den angivna`PreferredWidth` är lika i värde med strömmen`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Fungerar som en hashfunktion för denna typ. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Returnerar en användarvänlig sträng som visar värdet på detta objekt. |

## Fält

| namn | Beskrivning |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | Returnerar en instans som representerar värdet "föredragen bredd är inte angiven". |

## Anmärkningar

Önskad bredd kan anges i procent, antal poäng eller ett speciellt "ingen/auto"-värde.

Förekomsterna av denna klass är oföränderliga.

## Exempel

Visar hur du ställer in en tabell för att automatiskt anpassa till 50 % av sidans bredd.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

Visar hur man ställer in en föredragen bredd för tabellceller.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Det finns två sätt att tillämpa klassen "PreferredWidth" på tabellceller.
// 1 - Ställ in en absolut föredragen bredd baserat på punkter:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Ställ in en relativ föredragen bredd baserat på procent av tabellens bredd:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// En cell utan angiven önskad bredd kommer att ta upp resten av det tillgängliga utrymmet.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Varje konfiguration av egenskapen "PreferredWidth" skapar ett nytt objekt.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Se även

* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
