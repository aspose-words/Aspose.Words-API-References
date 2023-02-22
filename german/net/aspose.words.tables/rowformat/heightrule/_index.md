---
title: RowFormat.HeightRule
second_title: Aspose.Words für .NET-API-Referenz
description: RowFormat eigendom. Ruft die Regel zur Bestimmung der Höhe der Tabellenzeile ab oder legt sie fest.
type: docs
weight: 50
url: /de/net/aspose.words.tables/rowformat/heightrule/
---
## RowFormat.HeightRule property

Ruft die Regel zur Bestimmung der Höhe der Tabellenzeile ab oder legt sie fest.

```csharp
public HeightRule HeightRule { get; set; }
```

### Beispiele

Zeigt, wie Zeilen mit einem Document Builder formatiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Beginne eine zweite Reihe und konfiguriere dann ihre Höhe. Der Builder wendet diese Einstellungen auf an
// seine aktuelle Zeile sowie alle neuen Zeilen, die er danach erstellt.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// Die erste Zeile war von der Padding-Neukonfiguration nicht betroffen und enthält immer noch die Standardwerte.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

Zeigt, wie eine formatierte Tabelle mit DocumentBuilder erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Legen Sie einige Formatierungsoptionen für Text und Tabellendarstellung fest.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Wenn Sie die Formatierungsoptionen in einem Dokumentersteller konfigurieren, werden sie angewendet
// zur aktuellen Zelle/Zeile, in der sich der Cursor befindet,
// sowie alle neuen Zellen und Zeilen, die mit diesem Builder erstellt wurden.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Rekonfiguriere die Formatierungsobjekte des Builders für neue Zeilen und Zellen, die wir gleich erstellen werden.
// Der Builder wendet diese nicht auf die erste bereits erstellte Zeile an, damit sie als Kopfzeile hervorsticht.
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

* enum [HeightRule](../../../aspose.words/heightrule/)
* class [RowFormat](../)
* namensraum [Aspose.Words.Tables](../../rowformat/)
* Montage [Aspose.Words](../../../)


