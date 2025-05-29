---
title: DocumentBuilder.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentBuilder-Schriftart-Eigenschaft, um mühelos auf Ihre aktuelle Schriftformatierung zuzugreifen und sie anzupassen. Verbessern Sie noch heute den Stil Ihres Dokuments!
type: docs
weight: 100
url: /de/net/aspose.words/documentbuilder/font/
---
## DocumentBuilder.Font property

Gibt ein Objekt zurück, das die aktuellen Schriftformatierungseigenschaften darstellt.

```csharp
public Font Font { get; }
```

## Bemerkungen

Verwenden`Font` um auf die Schriftformatierungseigenschaften zuzugreifen und diese zu ändern.

Geben Sie die Schriftformatierung an, bevor Sie Text einfügen.

## Beispiele

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

* class [Font](../../font/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
