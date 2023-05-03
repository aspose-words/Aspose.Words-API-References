---
title: ImageSaveOptions.Scale
linktitle: Scale
second_title: Aspose.Words for .NET API Reference
description: ImageSaveOptions Scale property. Gets or sets the zoom factor for the generated images in C#.
type: docs
weight: 140
url: /net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Gets or sets the zoom factor for the generated images.

```csharp
public float Scale { get; set; }
```

## Remarks

The default value is 1.0. The value must be greater than 0.

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

Shows how to edit the image while Aspose.Words converts a document to one.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// edit the image while the saving operation renders it.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // We can adjust these properties to change the image's brightness and contrast.
    // Both are on a 0-1 scale and are at 0.5 by default.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // We can adjust horizontal and vertical resolution with these properties.
    // This will affect the dimensions of the image.
    // The default value for these properties is 96.0, for a resolution of 96dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // We can scale the image using this property. The default value is 1.0, for scaling of 100%.
    // We can use this property to negate any changes in image dimensions that changing the resolution would cause.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### See Also

* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../imagesaveoptions/)
* assembly [Aspose.Words](../../../)
