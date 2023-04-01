---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
second_title: Aspose.Words for .NET API Reference
description: ShapeBase property. Gets the size of the shape in points in C#.
type: docs
weight: 510
url: /net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Gets the size of the shape in points.

```csharp
public SizeF SizeInPoints { get; }
```

## Examples

Shows how to verify a shape's size and markup language.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
