---
title: TableStyle.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words for .NET
description: Discover the TableStyle Shading property to enhance your table cells with customizable shading formatting for a polished, professional look.
type: docs
weight: 120
url: /net/aspose.words/tablestyle/shading/
---
## TableStyle.Shading property

Gets a [`Shading`](../../shading/) object that refers to the shading formatting for table cells.

```csharp
public Shading Shading { get; }
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
Assert.That(table.Bidi, Is.True);
Assert.That(table.CellSpacing, Is.EqualTo(5.0d));
Assert.That(table.StyleName, Is.EqualTo("MyTableStyle1"));

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### See Also

* class [Shading](../../shading/)
* class [TableStyle](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
