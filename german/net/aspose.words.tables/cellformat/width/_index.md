---
title: CellFormat.Width
second_title: Aspose.Words für .NET-API-Referenz
description: CellFormat eigendom. Ermittelt die Breite der Zelle in Punkten.
type: docs
weight: 140
url: /de/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Ermittelt die Breite der Zelle in Punkten.

```csharp
public double Width { get; set; }
```

### Bemerkungen

Die Breite wird von Aspose.Words beim Laden und Speichern von Dokumenten berechnet. Derzeit wird nicht jede Kombination von Tabellen-, Zellen- und Dokumenteigenschaften unterstützt. Der zurückgegebene Wert ist für einige Dokumente möglicherweise nicht genau. Er stimmt möglicherweise nicht genau mit dem überein Zellenbreite, wie von MS Word berechnet, wenn das Dokument in MS Word geöffnet wird.

Das Festlegen dieser Eigenschaft wird nicht empfohlen. Es gibt keine Garantie dafür, dass die Zelle tatsächlich die festgelegte Breite hat. Die Breite kann angepasst werden, um Zellinhalte in einem automatisch angepassten Tabellenlayout zu berücksichtigen. Zellen in anderen Zeilen können eine widersprüchliche Breite haben Einstellungen. Die Größe der Tabelle kann geändert werden, damit sie in den Container passt oder den Tabellenbreiteneinstellungen entspricht. Erwägen Sie die Verwendung[`PreferredWidth`](../preferredwidth/) zum Festlegen der Zellenbreite. Festlegen dieser Eigenschaftssätze[`PreferredWidth`](../preferredwidth/)implizit seit Version 15.8.

### Beispiele

Zeigt, wie Zellen mit einem Document Builder formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Fügen Sie eine zweite Zelle ein und konfigurieren Sie dann die Optionen zum Auffüllen des Zellentexts.
// Der Builder wendet diese Einstellungen auf die aktuelle Zelle an und erstellt anschließend alle neuen Zellen.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// Die erste Zelle war von der Neukonfiguration der Auffüllung nicht betroffen und enthält weiterhin die Standardwerte.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// Die erste Zelle wird im Ausgabedokument weiterhin vergrößert, um der Größe der benachbarten Zelle zu entsprechen.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

Zeigt, wie man eine Tabelle mit benutzerdefinierten Rändern erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen Dokumentersteller
// wendet sie auf jede Zeile und Zelle an, die wir damit hinzufügen.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Wenn Sie die Formatierung ändern, wird sie auf die aktuelle Zelle angewendet.
// und alle neuen Zellen, die wir anschließend mit dem Builder erstellen.
// Dies hat keine Auswirkungen auf die Zellen, die wir zuvor hinzugefügt haben.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Zeilenhöhe erhöhen, um sie an den vertikalen Text anzupassen.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Siehe auch

* class [CellFormat](../)
* namensraum [Aspose.Words.Tables](../../cellformat/)
* Montage [Aspose.Words](../../../)


