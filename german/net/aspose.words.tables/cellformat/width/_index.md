---
title: CellFormat.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words für .NET
description: Entdecken Sie die CellFormat Width-Eigenschaft, um die Zellenbreite einfach in Punkten zu messen und so das Layout und die Lesbarkeit Ihrer Tabelle zu verbessern.
type: docs
weight: 140
url: /de/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Ruft die Breite der Zelle in Punkten ab.

```csharp
public double Width { get; set; }
```

## Bemerkungen

Die Breite wird von Aspose.Words beim Laden und Speichern des Dokuments berechnet. Derzeit wird nicht jede Kombination aus Tabellen-, Zellen- und Dokumenteigenschaften unterstützt. Der zurückgegebene Wert ist für einige Dokumente möglicherweise nicht genau. Er entspricht möglicherweise nicht genau der von MS Word berechneten Zellenbreite, wenn das Dokument in MS Word geöffnet wird.

Das Festlegen dieser Eigenschaft wird nicht empfohlen. Es gibt keine Garantie dafür, dass die Zelle tatsächlich die festgelegte Breite hat. Die Breite kann angepasst werden, um Zelleninhalte in einem automatisch angepassten Tabellenlayout unterzubringen. Zellen in anderen Zeilen haben möglicherweise widersprüchliche Breiteneinstellungen. Die Größe der Tabelle kann angepasst werden, um in den Container zu passen oder die Tabellenbreiteneinstellungen einzuhalten. Erwägen Sie die Verwendung[`PreferredWidth`](../preferredwidth/)zum Einstellen der Zellenbreite. Durch das Setzen dieser Eigenschaft wird[`PreferredWidth`](../preferredwidth/) implizit seit Version 15.8.

## Beispiele

Zeigt, wie Zellen mit einem Dokumentgenerator formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Fügen Sie eine zweite Zelle ein und konfigurieren Sie dann die Textauffüllungsoptionen für die Zelle.
// Der Builder wendet diese Einstellungen auf seine aktuelle Zelle und alle danach erstellten neuen Zellen an.
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

// Die erste Zelle war von der Neukonfiguration der Auffüllung nicht betroffen und enthält noch immer die Standardwerte.
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

// Die erste Zelle wird im Ausgabedokument weiterhin wachsen, um der Größe der benachbarten Zelle zu entsprechen.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

Zeigt, wie eine Tabelle mit benutzerdefinierten Rändern erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen Dokumentgenerator
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

// Das Ändern der Formatierung wird auf die aktuelle Zelle angewendet,
// und alle neuen Zellen, die wir anschließend mit dem Builder erstellen.
// Dies hat keine Auswirkungen auf die Zellen, die wir zuvor hinzugefügt haben.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Erhöhen Sie die Zeilenhöhe, damit der vertikale Text hineinpasst.
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
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
