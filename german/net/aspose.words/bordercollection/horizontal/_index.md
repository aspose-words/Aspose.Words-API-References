---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words für .NET
description: Entdecken Sie die horizontale BorderCollection-Eigenschaft für nahtlose Zell- und Absatzränder. Verbessern Sie Ihr Layout mit perfekter Ausrichtung und Stil!
type: docs
weight: 50
url: /de/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Ruft den horizontalen Rahmen ab, der zwischen Zellen oder übereinstimmenden Absätzen verwendet wird.

```csharp
public Border Horizontal { get; }
```

## Beispiele

Zeigt, wie Sie Einstellungen für horizontale Rahmen auf das Format eines Absatzes anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellt einen roten horizontalen Rahmen für den Absatz. Alle nachfolgenden Absätze übernehmen diese Rahmeneinstellungen.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Text in das Dokument schreiben, ohne anschließend einen neuen Absatz zu erstellen.
// Da sich darunter kein Absatz befindet, ist der horizontale Rahmen nicht sichtbar.
builder.Write("Paragraph above horizontal border.");

// Sobald wir einen zweiten Absatz hinzufügen, wird der Rand des ersten Absatzes sichtbar.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

Zeigt, wie Sie Einstellungen für vertikale Rahmen auf das Format einer Tabellenzeile anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Tabelle mit roten und blauen Innenrändern.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Passen Sie das Erscheinungsbild der Ränder an, die zwischen den Zeilen angezeigt werden.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Passen Sie das Erscheinungsbild der Rahmen an, die zwischen den Zellen angezeigt werden.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// Ein Zeilenformat und der innere Absatz einer Zelle verwenden unterschiedliche Rahmeneinstellungen.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### Siehe auch

* class [Border](../../border/)
* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
