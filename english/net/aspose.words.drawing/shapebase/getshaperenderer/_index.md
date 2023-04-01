---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
second_title: Aspose.Words for .NET API Reference
description: ShapeBase method. Creates and returns an object that can be used to render this shape into an image in C#.
type: docs
weight: 660
url: /net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Creates and returns an object that can be used to render this shape into an image.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Return Value

The renderer object for this shape.

## Remarks

This method just invokes the [`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) constructor and passes this object as a parameter.

## Examples

Shows how to use a shape renderer to export shapes to files in the local file system.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// There are 7 shapes in the document, including one group shape with 2 child shapes.
// We will render every shape to an image file in the local file system
// while ignoring the group shapes since they have no appearance.
// This will produce 6 image files.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### See Also

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
