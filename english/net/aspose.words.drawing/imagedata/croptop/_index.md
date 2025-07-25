---
title: ImageData.CropTop
linktitle: CropTop
articleTitle: CropTop
second_title: Aspose.Words for .NET
description: Optimize your images with ImageData CropTop, controlling picture removal from the top for perfect framing and enhanced visual appeal.
type: docs
weight: 90
url: /net/aspose.words.drawing/imagedata/croptop/
---
## ImageData.CropTop property

Defines the fraction of picture removal from the top side.

```csharp
public double CropTop { get; set; }
```

## Remarks

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

## Examples

Shows how to edit a shape's image data.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Import a shape from the source document and append it to the first paragraph.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.That(imageData.HasImage, Is.True);

// If an image has no borders, its ImageData object will define the border color as empty.
Assert.That(imageData.Borders.Count, Is.EqualTo(4));
Assert.That(imageData.Borders[0].Color, Is.EqualTo(Color.Empty));

// This image does not link to another shape or image file in the local file system.
Assert.That(imageData.IsLink, Is.False);
Assert.That(imageData.IsLinkOnly, Is.False);

// The "Brightness" and "Contrast" properties define image brightness and contrast
// on a 0-1 scale, with the default value at 0.5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// The above brightness and contrast values have created an image with a lot of white.
// We can select a color with the ChromaKey property to replace with transparency, such as white.
imageData.ChromaKey = Color.White;

// Import the source shape again and set the image to monochrome.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Import the source shape again to create a third image and set it to BiLevel.
// BiLevel sets every pixel to either black or white, whichever is closer to the original color.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Cropping is determined on a 0-1 scale. Cropping a side by 0.3
// will crop 30% of the image out at the cropped side.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### See Also

* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
