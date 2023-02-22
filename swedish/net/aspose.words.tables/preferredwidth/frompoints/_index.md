---
title: PreferredWidth.FromPoints
second_title: Aspose.Words för .NET API Referens
description: PreferredWidth metod. En skapandemetod som returnerar en ny instans som representerar en föredragen bredd som anges med ett antal punkter.
type: docs
weight: 30
url: /sv/net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

En skapandemetod som returnerar en ny instans som representerar en föredragen bredd som anges med ett antal punkter.

```csharp
public static PreferredWidth FromPoints(double points)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| points | Double | Värdet måste vara från 0 till 22 tum (22 * 72 poäng). |

### Exempel

Visar hur du använder enhetskonverteringsverktyg samtidigt som du anger en önskad bredd för en cell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(ConvertUtil.InchToPoint(3));
builder.InsertCell();

Assert.AreEqual(216.0d, table.FirstRow.FirstCell.CellFormat.PreferredWidth.Value);
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

* class [PreferredWidth](../)
* namnutrymme [Aspose.Words.Tables](../../preferredwidth/)
* hopsättning [Aspose.Words](../../../)


