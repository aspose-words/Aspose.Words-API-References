---
title: RowFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „RowFormat Height“, um die Zeilenhöhe von Tabellen einfach in Punkten anzupassen und so das Layout und die Lesbarkeit Ihres Dokuments zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.tables/rowformat/height/
---
## RowFormat.Height property

Ruft die Höhe der Tabellenzeile in Punkten ab oder legt sie fest.

```csharp
public double Height { get; set; }
```

## Beispiele

Zeigt, wie Zeilen mit einem Dokumentgenerator formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Starten Sie eine zweite Zeile und konfigurieren Sie dann deren Höhe. Der Builder wendet diese Einstellungen an auf
// seine aktuelle Zeile sowie alle neuen Zeilen, die es danach erstellt.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Die erste Zeile wurde durch die Neukonfiguration der Auffüllung nicht beeinflusst und enthält weiterhin die Standardwerte.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

Zeigt, wie mit DocumentBuilder eine formatierte Tabelle erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Legen Sie einige Formatierungsoptionen für die Text- und Tabellendarstellung fest.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Durch die Konfiguration der Formatierungsoptionen in einem Dokument-Generator werden diese angewendet
// zur aktuellen Zelle/Zeile, in der sich der Cursor befindet,
// sowie alle neuen Zellen und Zeilen, die mit diesem Builder erstellt wurden.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Konfigurieren Sie die Formatierungsobjekte des Builders für die neuen Zeilen und Zellen neu, die wir erstellen möchten.
// Der Builder wendet diese nicht auf die erste bereits erstellte Zeile an, sodass sie als Kopfzeile hervorsticht.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Siehe auch

* class [RowFormat](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
