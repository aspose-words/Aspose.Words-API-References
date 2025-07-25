---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words for .NET
description: Discover the Table HorizontalAnchor property to optimize floating table positioning. Easily customize horizontal alignment for enhanced layout control.
type: docs
weight: 170
url: /net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is Column.

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

## Examples

Shows how to work with floating tables properties.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.That(table.HorizontalAnchor, Is.EqualTo(RelativeHorizontalPosition.Margin));
    Assert.That(table.VerticalAnchor, Is.EqualTo(RelativeVerticalPosition.Paragraph));
    Assert.That(table.AllowOverlap, Is.EqualTo(false));

    // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### See Also

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
