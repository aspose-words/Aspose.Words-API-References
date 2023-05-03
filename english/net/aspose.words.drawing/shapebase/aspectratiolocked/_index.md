---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
second_title: Aspose.Words for .NET API Reference
description: ShapeBase AspectRatioLocked property. Specifies whether the shapes aspect ratio is locked in C#.
type: docs
weight: 40
url: /net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## AspectRatioLocked property

Specifies whether the shape's aspect ratio is locked.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Remarks

The default value depends on the [`ShapeType`](../../shapetype/), for the Image it is `true` but for the other shape types it is `false`.

Has effect for top level shapes only.

## Examples

Shows how to lock/unlock a shape's aspect ratio.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a shape. If we open this document in Microsoft Word, we can left click the shape to reveal
// eight sizing handles around its perimeter, which we can click and drag to change its size.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Set the "AspectRatioLocked" property to "true" to preserve the shape's aspect ratio
// when using any of the four diagonal sizing handles, which change both the image's height and width.
// Using any orthogonal sizing handles that either change the height or width will still change the aspect ratio.
// Set the "AspectRatioLocked" property to "false" to allow us to
// freely change the image's aspect ratio with all sizing handles.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
