---
title: PreferredWidth.Auto
linktitle: Auto
articleTitle: Auto
second_title: Aspose.Words für .NET
description: PreferredWidth Auto veld. Gibt eine Instanz zurück die den Wert Bevorzugte Breite ist nicht angegeben darstellt in C#.
type: docs
weight: 10
url: /de/net/aspose.words.tables/preferredwidth/auto/
---
## PreferredWidth.Auto field

Gibt eine Instanz zurück, die den Wert „Bevorzugte Breite ist nicht angegeben“ darstellt.

```csharp
public static readonly PreferredWidth Auto;
```

## Beispiele

Zeigt, wie man eine bevorzugte Breite für Tabellenzellen festlegt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Es gibt zwei Möglichkeiten, die Klasse „PreferredWidth“ auf Tabellenzellen anzuwenden.
// 1 – Legen Sie eine absolute bevorzugte Breite basierend auf Punkten fest:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 – Legen Sie eine relative bevorzugte Breite basierend auf dem Prozentsatz der Tabellenbreite fest:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Eine Zelle, für die keine bevorzugte Breite angegeben ist, nimmt den Rest des verfügbaren Platzes ein.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Jede Konfiguration der Eigenschaft „PreferredWidth“ erstellt ein neues Objekt.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Siehe auch

* class [PreferredWidth](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
