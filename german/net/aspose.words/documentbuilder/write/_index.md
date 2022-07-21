---
title: Write
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt einen String an der aktuellen Einfügeposition in das Dokument ein.
type: docs
weight: 620
url: /de/net/aspose.words/documentbuilder/write/
---
## DocumentBuilder.Write method

Fügt einen String an der aktuellen Einfügeposition in das Dokument ein.

```csharp
public void Write(string text)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| text | String | Die Zeichenfolge, die in das Dokument eingefügt werden soll. |

### Bemerkungen

Aktuelle Schriftartformatierung, die von angegeben wird[`Font`](../font)Eigenschaft wird verwendet.

### Beispiele

Zeigt, wie eine von einem Rahmen umgebene Zeichenfolge in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Zeigt, wie Sie mit einem Document Builder eine Tabelle erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Beginne die Tabelle und fülle dann die erste Zeile mit zwei Zellen.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Die "EndRow"-Methode des Builders aufrufen, um eine neue Zeile zu beginnen.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Zeigt, wie eine formatierte 2x2-Tabelle erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Beim Erstellen der Tabelle wendet der Document Builder seine aktuellen RowFormat/CellFormat-Eigenschaftswerte an
// zur aktuellen Zeile/Zelle, in der sich der Cursor befindet, und zu allen neuen Zeilen/Zellen, wenn sie erstellt werden.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Zuvor hinzugefügte Zeilen und Zellen sind nicht rückwirkend von Änderungen an der Formatierung des Builders betroffen.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
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

* class [DocumentBuilder](../../documentbuilder)
* namensraum [Aspose.Words](../../documentbuilder)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
