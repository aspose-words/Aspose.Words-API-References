---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: Aspose.Words for .NET API Reference
description: ImageSaveOptions PaperColor property. Gets or sets the background paper color for the generated images in C#.
type: docs
weight: 100
url: /net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Gets or sets the background (paper) color for the generated images.

The default value is White.

```csharp
public Color PaperColor { get; set; }
```

## Remarks

When rendering pages of a document that specifies its own background color, then the document background color will override the color specified by this property.

## Examples

Renders a page of a Word document into an image with transparent or colored background.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Set the "PaperColor" property to a transparent color to apply a transparent
// background to the document while rendering it to an image.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Set the "PaperColor" property to an opaque color to apply that color
// as the background of the document as we render it to an image.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### See Also

* class [ImageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../imagesaveoptions/)
* assembly [Aspose.Words](../../../)
