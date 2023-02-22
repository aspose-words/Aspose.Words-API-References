---
title: CellFormat.PreferredWidth
second_title: Aspose.Words für .NET-API-Referenz
description: CellFormat eigendom. Gibt die bevorzugte Breite der Zelle zurück oder legt sie fest.
type: docs
weight: 70
url: /de/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Gibt die bevorzugte Breite der Zelle zurück oder legt sie fest.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

### Bemerkungen

Die bevorzugte Breite (zusammen mit der Option Automatische Anpassung der Tabelle) bestimmt, wie die tatsächliche -Breite der Zelle vom Tabellenlayoutalgorithmus berechnet wird. Das Tabellenlayout kann von Aspose.Words ausgeführt werden, wenn es das Dokument speichert, oder von Microsoft Word, wenn es das Dokument anzeigt.

Die bevorzugte Breite kann in Punkten oder in Prozent angegeben werden. Die bevorzugte Breite kann auch als „auto“ angegeben werden, was bedeutet, dass keine bevorzugte Breite angegeben wird.

Der Standardwert ist[`Auto`](../../preferredwidth/auto/).

### Beispiele

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* namensraum [Aspose.Words.Tables](../../cellformat/)
* Montage [Aspose.Words](../../../)


