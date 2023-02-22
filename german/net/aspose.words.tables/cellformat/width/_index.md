---
title: CellFormat.Width
second_title: Aspose.Words für .NET-API-Referenz
description: CellFormat eigendom. Ruft die Breite der Zelle in Punkten ab.
type: docs
weight: 130
url: /de/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Ruft die Breite der Zelle in Punkten ab.

```csharp
public double Width { get; set; }
```

### Bemerkungen

Die Breite wird von Aspose.Words beim Laden und Speichern des Dokuments berechnet. Derzeit wird nicht jede Kombination von Tabellen-, Zellen- und Dokumenteigenschaften unterstützt. Der zurückgegebene Wert ist möglicherweise für einige Dokumente nicht genau. Er stimmt möglicherweise nicht genau mit dem überein Zellenbreite wie von MS Word berechnet, wenn das Dokument in MS Word geöffnet wird.

Das Festlegen dieser Eigenschaft wird nicht empfohlen. Es gibt keine Garantie dafür, dass die Zelle tatsächlich die festgelegte Breite hat. Die Breite kann angepasst werden, um Zellinhalte in einem automatisch angepassten Tabellenlayout aufzunehmen. Zellen in anderen Zeilen können widersprüchliche Breiten haben settings. Die Größe der Tabelle kann geändert werden, damit sie in den Container passt oder den Einstellungen für die Tabellenbreite entspricht. Erwägen Sie die Verwendung[`PreferredWidth`](../preferredwidth/) zum Festlegen der Zellenbreite. Festlegen dieser Eigenschaftssätze[`PreferredWidth`](../preferredwidth/)implizit seit Version 15.8.

### Beispiele

Zeigt, wie Zellen mit einem Document Builder formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Eine zweite Zelle einfügen und dann Optionen zum Auffüllen des Zelltextes konfigurieren.
// Der Builder wendet diese Einstellungen auf seine aktuelle Zelle an und erstellt danach alle neuen Zellen.
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

// Die erste Zelle war von der Padding-Neukonfiguration nicht betroffen und enthält immer noch die Standardwerte.
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

// Die erste Zelle wird im Ausgabedokument immer noch größer, um sie an die Größe der benachbarten Zelle anzupassen.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

Zeigt, wie eine Tabelle mit benutzerdefinierten Rahmen erstellt wird.

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

// Wenn Sie die Formatierung ändern, wird sie auf die aktuelle Zelle angewendet,
// und alle neuen Zellen, die wir danach mit dem Builder erstellen.
// Dies wirkt sich nicht auf die zuvor hinzugefügten Zellen aus.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Erhöhen Sie die Zeilenhöhe, um sie an den vertikalen Text anzupassen.
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


