---
title: ConditionalStyleType Enum
linktitle: ConditionalStyleType
articleTitle: ConditionalStyleType
second_title: Aspose.Words for .NET
description: Aspose.Words.ConditionalStyleType enum. Represents possible table areas to which conditional formatting may be defined in a table style in C#.
type: docs
weight: 410
url: /net/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enumeration

Represents possible table areas to which conditional formatting may be defined in a table style.

```csharp
public enum ConditionalStyleType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| FirstRow | `0` | Specifies formatting of the first row of a table. |
| FirstColumn | `1` | Specifies formatting of the first column of a table. |
| LastRow | `2` | Specifies formatting of the last row of a table. |
| LastColumn | `3` | Specifies formatting of the last column of a table. |
| OddRowBanding | `4` | Specifies formatting of odd-numbered row stripe. |
| OddColumnBanding | `5` | Specifies formatting of odd-numbered column stripe. |
| EvenRowBanding | `6` | Specifies formatting of even-numbered row stripe. |
| EvenColumnBanding | `7` | Specifies formatting of even-numbered column stripe. |
| TopLeftCell | `8` | Specifies formatting of the top left cell of a table. |
| TopRightCell | `9` | Specifies formatting of the top right cell of a table. |
| BottomLeftCell | `10` | Specifies formatting of the bottom left cell of a table. |
| BottomRightCell | `11` | Specifies formatting of the bottom right cell of a table. |

## Examples

Shows how to work with certain area styles of a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Create a custom table style.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Conditional styles are formatting changes that affect only some of the table's cells
// based on a predicate, such as the cells being in the last row.
// Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
// 1 -  By style type:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 -  By index:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 -  As a property:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Apply padding and text formatting to conditional styles.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// List all possible style conditions.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Apply the custom style, which contains all conditional styles, to the table.
table.Style = tableStyle;

// Our style applies some conditional styles by default.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// We will need to enable all other styles ourselves via the "StyleOptions" property.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
