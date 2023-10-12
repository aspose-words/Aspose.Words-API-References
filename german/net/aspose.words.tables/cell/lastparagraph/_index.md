---
title: Cell.LastParagraph
second_title: Aspose.Words für .NET-API-Referenz
description: Cell eigendom. Ruft den letzten Absatz unter den unmittelbar untergeordneten Elementen ab.
type: docs
weight: 60
url: /de/net/aspose.words.tables/cell/lastparagraph/
---
## Cell.LastParagraph property

Ruft den letzten Absatz unter den unmittelbar untergeordneten Elementen ab.

```csharp
public Paragraph LastParagraph { get; }
```

### Beispiele

Zeigt, wie Einstellungen für vertikale Ränder auf das Format einer Tabellenzeile angewendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstelle eine Tabelle mit roten und blauen Innenrändern.
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

    // Passen Sie das Erscheinungsbild der Ränder an, die zwischen den Zellen angezeigt werden.
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* namensraum [Aspose.Words.Tables](../../cell/)
* Montage [Aspose.Words](../../../)


