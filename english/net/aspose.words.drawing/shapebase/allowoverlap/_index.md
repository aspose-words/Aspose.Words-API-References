---
title: ShapeBase.AllowOverlap
second_title: Aspose.Words for .NET API Reference
description: ShapeBase property. Gets or sets a value that specifies whether this shape can overlap other shapes in C#.
type: docs
weight: 10
url: /net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Gets or sets a value that specifies whether this shape can overlap other shapes.

```csharp
public bool AllowOverlap { get; set; }
```

## Remarks

This property affects behavior of the shape in Microsoft Word. Aspose.Words ignores the value of this property.

This property is applicable only to top level shapes.

The default value is `true`.

## Examples

Shows how to work with floating tables properties.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
