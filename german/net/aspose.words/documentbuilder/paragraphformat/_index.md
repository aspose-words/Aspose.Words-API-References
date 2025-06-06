---
title: DocumentBuilder.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words für .NET
description: Erkunden Sie die ParagraphFormat-Eigenschaft von DocumentBuilder, um auf wichtige Funktionen zur Absatzformatierung zuzugreifen und diese anzupassen, um die Dokumentgestaltung zu verbessern.
type: docs
weight: 170
url: /de/net/aspose.words/documentbuilder/paragraphformat/
---
## DocumentBuilder.ParagraphFormat property

Gibt ein Objekt zurück, das die aktuellen Absatzformatierungseigenschaften darstellt.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## Beispiele

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

* class [ParagraphFormat](../../paragraphformat/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
