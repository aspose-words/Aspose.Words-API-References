---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words for .NET
description: Discover the ShapeBase SizeInPoints property to easily retrieve and manage shape dimensions in points for precise design control.
type: docs
weight: 540
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

Assert.That(shape.MarkupLanguage, Is.EqualTo(ShapeMarkupLanguage.Dml));
Assert.That(shape.SizeInPoints, Is.EqualTo(new SizeF(300, 300)));
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
