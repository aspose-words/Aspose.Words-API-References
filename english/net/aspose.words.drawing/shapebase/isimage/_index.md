---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words for .NET
description: Discover if a shape is an image with ShapeBase's IsImage property. Easily identify image shapes for enhanced design flexibility and functionality.
type: docs
weight: 300
url: /net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

Returns `true` if this shape is an image shape.

```csharp
public bool IsImage { get; }
```

## Examples

Shows how to open an HTML document with images from a stream using a base URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Pass the URI of the base folder while loading it
    // so that any images with relative URIs in the HTML document can be found.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verify that the first shape of the document contains a valid image.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.That(shape.IsImage, Is.True);
    Assert.That(shape.ImageData.ImageBytes, Is.Not.Null);
    Assert.That(ConvertUtil.PointToPixel(shape.Width), Is.EqualTo(32.0).Within(0.01));
    Assert.That(ConvertUtil.PointToPixel(shape.Height), Is.EqualTo(32.0).Within(0.01));
}
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
