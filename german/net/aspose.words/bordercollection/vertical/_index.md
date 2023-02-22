---
title: BorderCollection.Vertical
second_title: Aspose.Words für .NET-API-Referenz
description: BorderCollection eigendom. Ruft den vertikalen Rahmen ab der zwischen Zellen verwendet wird.
type: docs
weight: 130
url: /de/net/aspose.words/bordercollection/vertical/
---
## BorderCollection.Vertical property

Ruft den vertikalen Rahmen ab, der zwischen Zellen verwendet wird.

```csharp
public Border Vertical { get; }
```

### Beispiele

Zeigt, wie Einstellungen für vertikale Rahmen auf das Format einer Tabellenzeile angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Tabelle mit roten und blauen inneren Rändern.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Passen Sie das Erscheinungsbild der Grenzen an, die zwischen den Zeilen erscheinen.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Passen Sie das Aussehen der Grenzen an, die zwischen den Zellen erscheinen.
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
* namensraum [Aspose.Words](../../bordercollection/)
* Montage [Aspose.Words](../../../)


