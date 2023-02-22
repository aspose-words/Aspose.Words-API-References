---
title: HorizontalAlignment
second_title: Aspose.Words for .NET API Reference
description: ShapeBase property. Specifies how the shape is positioned horizontally in C#.
type: docs
weight: 210
url: /net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Specifies how the shape is positioned horizontally.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

## Remarks

The default value is None.

Has effect only for top level floating shapes.

## Examples

Shows how to insert a floating image to the center of a page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### See Also

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
