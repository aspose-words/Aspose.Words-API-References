---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words for .NET
description: Discover the Table AllowOverlap property, which controls whether floating objects can overlap your table. Enhance layout flexibility for better document presentation.
type: docs
weight: 70
url: /net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is `true`.

```csharp
public bool AllowOverlap { get; }
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

* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
