---
title: Class ImageData
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.ImageData class. Defines an image for a shape in C#.
type: docs
weight: 930
url: /net/aspose.words.drawing/imagedata/
---
## ImageData class

Defines an image for a shape.

To learn more, visit the [Working with Images](https://docs.aspose.com/words/net/working-with-images/) documentation article.

```csharp
public class ImageData
```

## Properties

| Name | Description |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Determines whether an image will be displayed in black and white. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Gets the collection of borders of the image. Borders only have effect for inline images. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Gets or sets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Defines the color value of the image that will be treated as transparent. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Gets or sets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Defines the fraction of picture removal from the bottom side. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Defines the fraction of picture removal from the left side. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Defines the fraction of picture removal from the right side. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Defines the fraction of picture removal from the top side. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Determines whether a picture will display in grayscale mode. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Returns `true` if the shape has image bytes or links an image. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Gets or sets the raw bytes of the image stored in the shape. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Gets the information about image size and resolution. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Gets the type of the image. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Returns `true` if the image is linked to the shape (when [`SourceFullName`](./sourcefullname/) is specified). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Returns `true` if the image is linked and not stored in the document. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Gets or sets the path and name of the source file for the linked image. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Defines the title of an image. |

## Methods

| Name | Description |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(Stream) | Saves the image into the specified stream. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(string) | Saves the image into a file. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(Image) | Sets the image that the shape displays. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(Stream) | Sets the image that the shape displays. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(string) | Sets the image that the shape displays. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Returns image bytes for any image regardless whether the image is stored or linked. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Gets the image stored in the shape as a Image object. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Creates and returns a stream that contains the image bytes. |

## Remarks

Use the [`ImageData`](../shape/imagedata/) property to access and modify the image inside a shape. You do not create instances of the `ImageData` class directly.

An image can be stored inside a shape, linked to external file or both (linked and stored in the document).

Regardless of whether the image is stored inside the shape or linked, you can always access the actual image using the [`ToByteArray`](./tobytearray/), [`ToStream`](./tostream/), [`ToImage`](./toimage/) or [`Save`](./save/) methods. If the image is stored inside the shape, you can also directly access it using the [`ImageBytes`](./imagebytes/) property.

To store an image inside a shape use the [`SetImage`](./setimage/) method. To link an image to a shape, set the [`SourceFullName`](./sourcefullname/) property.

## Examples

Shows how to extract images from a document, and save them to the local file system as individual files.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

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
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

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
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
