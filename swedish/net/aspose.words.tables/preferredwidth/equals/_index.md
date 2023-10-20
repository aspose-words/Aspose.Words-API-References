---
title: PreferredWidth.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words för .NET
description: PreferredWidth Equals metod. Bestämmer om den angivnaPreferredWidth är lika i värde med strömmenPreferredWidth  i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.tables/preferredwidth/equals/
---
## Equals(*[PreferredWidth](../)*) {#equals}

Bestämmer om den angivna[`PreferredWidth`](../) är lika i värde med strömmen[`PreferredWidth`](../) .

```csharp
public bool Equals(PreferredWidth other)
```

## Exempel

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
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

Bestämmer om det angivna objektet har samma värde som det aktuella objektet.

```csharp
public override bool Equals(object obj)
```

## Exempel

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
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
