---
title: BorderCollection.Top
linktitle: Top
articleTitle: Top
second_title: Aspose.Words für .NET
description: BorderCollection Top eigendom. Ruft den oberen Rand ab in C#.
type: docs
weight: 120
url: /de/net/aspose.words/bordercollection/top/
---
## BorderCollection.Top property

Ruft den oberen Rand ab.

```csharp
public Border Top { get; }
```

## Beispiele

Zeigt, wie Sie beim Erstellen einer Tabelle Rahmen- und Schattierungsfarben anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Tabelle starten und eine Standardfarbe/-stärke für ihre Ränder festlegen.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Erstelle eine Zeile mit zwei Zellen mit unterschiedlichen Hintergrundfarben.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Zellenformatierung zurücksetzen, um die Hintergrundfarben zu deaktivieren
// Legen Sie eine benutzerdefinierte Rahmenstärke für alle neuen Zellen fest, die vom Builder erstellt wurden.
// dann baue eine zweite Reihe.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Siehe auch

* class [Border](../../border/)
* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
