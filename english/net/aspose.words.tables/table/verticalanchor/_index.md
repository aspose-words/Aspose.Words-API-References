---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words for .NET
description: Discover the Table VerticalAnchor property to optimize floating table positioning. Learn how to enhance layout control with its default Margin value.
type: docs
weight: 340
url: /net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Gets the base object from which the vertical positioning of floating table should be calculated. Default value is Margin.

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
