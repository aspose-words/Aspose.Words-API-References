---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.ConditionalStyleCollection class. Represents a collection of ConditionalStyle objects in C#.
type: docs
weight: 410
url: /net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Represents a collection of [`ConditionalStyle`](../conditionalstyle/) objects.

To learn more, visit the [Working with Tables](https://docs.aspose.com/words/net/working-with-tables/) documentation article.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Properties

| Name | Description |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Gets the bottom left cell style. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Gets the bottom right cell style. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Gets the number of conditional styles in the collection. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Gets the even column banding style. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Gets the even row banding style. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Gets the first column style. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Gets the first row style. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Retrieves a [`ConditionalStyle`](../conditionalstyle/) object by conditional style type. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Gets the last column style. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Gets the last row style. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Gets the odd column banding style. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Gets the odd row banding style. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Gets the top left cell style. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Gets the top right cell style. |

## Methods

| Name | Description |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Clears all conditional styles of the table style. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all conditional styles in the collection. |

## Remarks

It is not possible to add or remove items from this collection. It contains permanent set of items: one item for each value of the [`ConditionalStyleType`](../conditionalstyletype/) enumeration type.

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

* class [ConditionalStyle](../conditionalstyle/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
