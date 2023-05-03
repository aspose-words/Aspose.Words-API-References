---
title: TableStyle.RowStripe
linktitle: RowStripe
articleTitle: RowStripe
second_title: Aspose.Words for .NET API Reference
description: TableStyle RowStripe property. Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding in C#.
type: docs
weight: 120
url: /net/aspose.words/tablestyle/rowstripe/
---
## TableStyle.RowStripe property

Gets or sets a number of rows to include in the banding when the style specifies odd/even row banding.

```csharp
public int RowStripe { get; set; }
```

## Examples

Shows how to create conditional table styles that alternate between rows.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// We can configure a conditional style of a table to apply a different color to the row/column,
// based on whether the row/column is even or odd, creating an alternating color pattern.
// We can also apply a number n to the row/column banding,
// meaning that the color alternates after every n rows/columns instead of one.
// Create a table where single columns and rows will band the columns will banded in threes.
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// Apply a line style to all the borders of the table.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// Set the two colors, which will alternate over every 3 rows.
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// Set a color to apply to every even column, which will override any custom row coloring.
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// The "StyleOptions" property enables row banding by default.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// Use the "StyleOptions" property also to enable column banding.
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### See Also

* class [TableStyle](../)
* namespace [Aspose.Words](../../tablestyle/)
* assembly [Aspose.Words](../../../)
