---
title: ImageData.Contrast
linktitle: Contrast
articleTitle: Contrast
second_title: Aspose.Words for .NET
description: Adjust image contrast easily with the ImageData Contrast property. Set values from 0.0 (low) to 1.0 (high) for optimal picture clarity and quality.
type: docs
weight: 50
url: /net/aspose.words.drawing/imagedata/contrast/
---
## ImageData.Contrast property

Gets or sets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast).

```csharp
public double Contrast { get; set; }
```

## Remarks

The default value is 0.5.

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
