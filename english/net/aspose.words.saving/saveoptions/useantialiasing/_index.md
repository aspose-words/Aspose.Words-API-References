---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words for .NET
description: Discover the SaveOptions UseAntiAliasing property to enhance your rendering quality. Control antialiasing for smoother visuals and improved performance.
type: docs
weight: 200
url: /net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Gets or sets a value determining whether or not to use anti-aliasing for rendering.

```csharp
public bool UseAntiAliasing { get; set; }
```

## Remarks

The default value is `false`. When this value is set to `true` anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: Tiff, Png, Bmp, Jpeg, Emf. When the document is exported to the Html, Mhtml, Epub, Azw3 or Mobi formats this option is used for raster images.

## Examples

Shows how to improve the quality of a rendered document with SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
