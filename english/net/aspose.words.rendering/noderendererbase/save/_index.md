---
title: NodeRendererBase.Save
second_title: Aspose.Words for .NET API Reference
description: NodeRendererBase method. Renders the shape into an image and saves into a file in C#.
type: docs
weight: 90
url: /net/aspose.words.rendering/noderendererbase/save/
---
## Save(string, ImageSaveOptions) {#save_1}

Renders the shape into an image and saves into a file.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| saveOptions | ImageSaveOptions | Specifies the options that control how the shape is rendered and saved. Can be `null`. |

## Examples

Shows how to render an Office Math object into an image file in the local file system.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
// how it renders the OfficeMath node into an image.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Set the "Scale" property to 5 to render the object to five times its original size.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* namespace [Aspose.Words.Rendering](../../noderendererbase/)
* assembly [Aspose.Words](../../../)

---

## Save(Stream, ImageSaveOptions) {#save}

Renders the shape into an image and saves into a stream.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream where to save the image of the shape. |
| saveOptions | ImageSaveOptions | Specifies the options that control how the shape is rendered and saved. Can be `null`. If this is `null`, the image will be saved in the PNG format. |

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

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* namespace [Aspose.Words.Rendering](../../noderendererbase/)
* assembly [Aspose.Words](../../../)
