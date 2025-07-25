---
title: Shape.ImageData
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words for .NET
description: Access and manage shape images effortlessly with the Shape ImageData property. Get instant results or null if not applicable. Enhance your design workflow!
type: docs
weight: 120
url: /net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

Provides access to the image of the shape. Returns `null` if the shape cannot have an image.

```csharp
public ImageData ImageData { get; }
```

## Examples

Shows how to extract images from a document, and save them to the local file system as individual files.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.That(shapes.Count(s => ((Shape)s).HasImage), Is.EqualTo(9));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // The image data of shapes may contain images of many possible image formats. 
        // We can determine a file extension for each image automatically, based on its format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Shows how to insert a linked image into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Below are two ways of applying an image to a shape so that it can display it.
// 1 -  Set the shape to contain the image.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Every image that we store in shape will increase the size of our document.
Assert.That(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length, Is.True);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 -  Set the shape to link to an image file in the local file system.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Linking to images will save space and result in a smaller document.
// However, the document can only display the image correctly while
// the image file is present at the location that the shape's "SourceFullName" property points to.
Assert.That(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length, Is.True);
```

### See Also

* class [ImageData](../../imagedata/)
* class [Shape](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
