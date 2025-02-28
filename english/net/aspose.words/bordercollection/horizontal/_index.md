---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words for .NET
description: Discover the BorderCollection Horizontal property for seamless cell and paragraph borders. Enhance your layout with perfect alignment and style!
type: docs
weight: 50
url: /net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Gets the horizontal border that is used between cells or conforming paragraphs.

```csharp
public Border Horizontal { get; }
```

## Examples

Shows how to apply settings to horizontal borders to a paragraph's format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a red horizontal border for the paragraph. Any paragraphs created afterwards will inherit these border settings.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Write text to the document without creating a new paragraph afterward.
// Since there is no paragraph underneath, the horizontal border will not be visible.
builder.Write("Paragraph above horizontal border.");

// Once we add a second paragraph, the border of the first paragraph will become visible.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

Shows how to apply settings to vertical borders to a table row's format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a table with red and blue inner borders.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Adjust the appearance of borders that will appear between rows.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Adjust the appearance of borders that will appear between cells.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// A row format, and a cell's inner paragraph use different border settings.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### See Also

* class [Border](../../border/)
* class [BorderCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
