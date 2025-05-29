---
title: PreferredWidth.Auto
linktitle: Auto
articleTitle: Auto
second_title: Aspose.Words för .NET
description: Upptäck fältet PreferredWidth Auto, som effektivt hanterar ospecificerade breddvärden för optimal layoutanpassning i dina projekt.
type: docs
weight: 10
url: /sv/net/aspose.words.tables/preferredwidth/auto/
---
## PreferredWidth.Auto field

Returnerar en instans som representerar värdet "föredragen bredd är inte angiven".

```csharp
public static readonly PreferredWidth Auto;
```

## Exempel

Visar hur man anger en önskad bredd för tabellceller.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Det finns två sätt att tillämpa klassen "PreferredWidth" på tabellceller.
// 1 - Ange en absolut önskad bredd baserat på punkter:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Ange en relativ önskad bredd baserat på procentandel av tabellens bredd:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// En cell utan specificerad önskad bredd kommer att ta upp resten av det tillgängliga utrymmet.
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
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
