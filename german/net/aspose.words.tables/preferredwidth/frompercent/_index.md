---
title: PreferredWidth.FromPercent
second_title: Aspose.Words für .NET-API-Referenz
description: PreferredWidth methode. Eine Erstellungsmethode die eine neue Instanz zurückgibt die eine als Prozentsatz angegebene bevorzugte Breite darstellt.
type: docs
weight: 20
url: /de/net/aspose.words.tables/preferredwidth/frompercent/
---
## PreferredWidth.FromPercent method

Eine Erstellungsmethode, die eine neue Instanz zurückgibt, die eine als Prozentsatz angegebene bevorzugte Breite darstellt.

```csharp
public static PreferredWidth FromPercent(double percent)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| percent | Double | Der Wert muss zwischen 0 und 100 liegen. |

### Beispiele

Zeigt, wie eine Tabelle so eingestellt wird, dass sie automatisch an 50 % der Seitenbreite angepasst wird.

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

Zeigt, wie Sie eine bevorzugte Breite für Tabellenzellen festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Es gibt zwei Möglichkeiten, die Klasse "PreferredWidth" auf Tabellenzellen anzuwenden.
// 1 - Stellen Sie eine absolute bevorzugte Breite basierend auf Punkten ein:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Legen Sie eine relative bevorzugte Breite basierend auf dem Prozentsatz der Tabellenbreite fest:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Eine Zelle ohne angegebene bevorzugte Breite nimmt den Rest des verfügbaren Platzes ein.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Jede Konfiguration der Eigenschaft "PreferredWidth" erzeugt ein neues Objekt.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Siehe auch

* class [PreferredWidth](../)
* namensraum [Aspose.Words.Tables](../../preferredwidth/)
* Montage [Aspose.Words](../../../)


