---
title: ConditionalStyle Class
linktitle: ConditionalStyle
articleTitle: ConditionalStyle
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.ConditionalStyle class for advanced table formatting. Enhance your documents with dynamic styles and improve readability effortlessly.
type: docs
weight: 500
url: /net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Represents special formatting applied to some area of a table with assigned table style.

To learn more, visit the [Working with Tables](https://docs.aspose.com/words/net/working-with-tables/) documentation article.

```csharp
public sealed class ConditionalStyle
```

## Properties

| Name | Description |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Gets the collection of default cell borders for the conditional style. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Gets or sets the amount of space (in points) to add below the contents of table cells. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Gets the character formatting of the conditional style. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Gets or sets the amount of space (in points) to add to the left of the contents of table cells. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Gets the paragraph formatting of the conditional style. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Gets or sets the amount of space (in points) to add to the right of the contents of table cells. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | Gets a [`Shading`](../shading/) object that refers to the shading formatting for this conditional style. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Gets or sets the amount of space (in points) to add above the contents of table cells. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Gets table area to which this conditional style relates. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Clears formatting of this conditional style. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(*object*) | Compares this conditional style with the specified object. |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Calculates hash code for this object. |

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
Assert.That(tableStyle.ConditionalStyles[0].Type, Is.EqualTo(ConditionalStyleType.FirstRow));

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
Assert.That(table.StyleOptions, Is.EqualTo(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands));

// We will need to enable all other styles ourselves via the "StyleOptions" property.
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
