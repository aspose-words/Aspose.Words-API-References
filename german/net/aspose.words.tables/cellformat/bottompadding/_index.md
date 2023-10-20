---
title: CellFormat.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words für .NET
description: CellFormat BottomPadding eigendom. Gibt den Abstand in Punkten zurück der unter dem Inhalt der Zelle hinzugefügt werden soll oder legt diesen fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.tables/cellformat/bottompadding/
---
## CellFormat.BottomPadding property

Gibt den Abstand (in Punkten) zurück, der unter dem Inhalt der Zelle hinzugefügt werden soll, oder legt diesen fest.

```csharp
public double BottomPadding { get; set; }
```

## Beispiele

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

### Siehe auch

* class [CellFormat](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
