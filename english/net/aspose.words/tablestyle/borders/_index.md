---
title: TableStyle.Borders
linktitle: Borders
second_title: Aspose.Words for .NET API Reference
description: TableStyle Borders property. Gets the collection of default cell borders for the style in C#.
type: docs
weight: 40
url: /net/aspose.words/tablestyle/borders/
---
## TableStyle.Borders property

Gets the collection of default cell borders for the style.

```csharp
public BorderCollection Borders { get; }
```

## Examples

Shows how to create custom style settings for the table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Setting the style properties of a table may affect the properties of the table itself.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### See Also

* class [BorderCollection](../../bordercollection/)
* class [TableStyle](../)
* namespace [Aspose.Words](../../tablestyle/)
* assembly [Aspose.Words](../../../)
