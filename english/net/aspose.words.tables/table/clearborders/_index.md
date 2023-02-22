---
title: ClearBorders
second_title: Aspose.Words for .NET API Reference
description: Table method. Removes all table and cell borders on this table in C#.
type: docs
weight: 370
url: /net/aspose.words.tables/table/clearborders/
---
## Table.ClearBorders method

Removes all table and cell borders on this table.

```csharp
public void ClearBorders()
```

## Examples

Shows how to apply an outline border to a table.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Align the table to the center of the page.
table.Alignment = TableAlignment.Center;

// Clear any existing borders and shading from the table.
table.ClearBorders();
table.ClearShading();

// Add green borders to the outline of the table.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Fill the cells with a light green solid color.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

Shows how to remove all borders from a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

// Modify the color and thickness of the top border.
Border topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];
table.SetBorder(BorderType.Top, LineStyle.Double, 1.5, Color.Red, true);

Assert.AreEqual(1.5d, topBorder.LineWidth);
Assert.AreEqual(Color.Red.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.Double, topBorder.LineStyle);

// Clear the borders of all cells in the table, and then save the document.
table.ClearBorders();

// Verify the values of the table's properties after re-opening the document.
doc = new Document(ArtifactsDir + "Table.ClearBorders.docx");
table = doc.FirstSection.Body.Tables[0];
topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];

Assert.AreEqual(0.0d, topBorder.LineWidth);
Assert.AreEqual(Color.Empty.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.None, topBorder.LineStyle);
```

### See Also

* class [Table](../)
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
