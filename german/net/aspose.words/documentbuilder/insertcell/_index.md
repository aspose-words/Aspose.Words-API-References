---
title: DocumentBuilder.InsertCell
linktitle: InsertCell
articleTitle: InsertCell
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der InsertCell-Methode von DocumentBuilder – fügen Sie schnell anpassbare Tabellenzellen hinzu, um die Organisation und Übersichtlichkeit zu verbessern.
type: docs
weight: 270
url: /de/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

Fügt eine Tabellenzelle in das Dokument ein.

```csharp
public Cell InsertCell()
```

### Rückgabewert

Der Zellknoten, der gerade eingefügt wurde.

## Bemerkungen

Um einen Tisch zu eröffnen, rufen Sie einfach an`InsertCell` . Danach werden alle Inhalte, die Sie mit anderen Methoden der[`DocumentBuilder`](../) Klasse wird zur aktuellen Zelle hinzugefügt.

Um eine neue Zelle in der gleichen Zeile zu beginnen, rufen Sie`InsertCell` wieder.

So beenden Sie einen Tabellenzeilenaufruf[`EndRow`](../endrow/).

Verwenden Sie die[`CellFormat`](../cellformat/) -Eigenschaft zum Festlegen der Zellenformatierung.

## Beispiele

Zeigt, wie Sie mit einem Dokumentgenerator eine Tabelle erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Starten Sie die Tabelle und füllen Sie dann die erste Zeile mit zwei Zellen.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Rufen Sie die Methode „EndRow“ des Builders auf, um eine neue Zeile zu beginnen.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
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

* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
