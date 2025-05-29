---
title: PreferredWidth.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „PreferredWidth ToString“, die eine benutzerfreundliche Zeichenfolge generiert, die den Wert Ihres Objekts für mehr Klarheit und Benutzerfreundlichkeit darstellt.
type: docs
weight: 80
url: /de/net/aspose.words.tables/preferredwidth/tostring/
---
## PreferredWidth.ToString method

Gibt eine benutzerfreundliche Zeichenfolge zurück, die den Wert dieses Objekts anzeigt.

```csharp
public override string ToString()
```

## Beispiele

Zeigt, wie Sie eine bevorzugte Breite für Tabellenzellen festlegen.

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

// Eine Zelle ohne angegebene bevorzugte Breite nimmt den restlichen verfügbaren Platz ein.
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
