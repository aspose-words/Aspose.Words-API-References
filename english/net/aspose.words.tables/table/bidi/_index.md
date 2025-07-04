---
title: Table.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words for .NET
description: Discover Table Bidi properties for seamless right-to-left table formatting. Enhance your web design with easy customization options!
type: docs
weight: 80
url: /net/aspose.words.tables/table/bidi/
---
## Table.Bidi property

Gets or sets whether this is a right-to-left table.

```csharp
public bool Bidi { get; set; }
```

## Remarks

When `true`, the cells in this row are laid out right to left.

The default value is `false`.

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

* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
