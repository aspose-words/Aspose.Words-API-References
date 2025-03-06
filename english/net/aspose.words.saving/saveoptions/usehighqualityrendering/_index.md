---
title: SaveOptions.UseHighQualityRendering
linktitle: UseHighQualityRendering
articleTitle: UseHighQualityRendering
second_title: Aspose.Words for .NET
description: Optimize your SaveOptions with the UseHighQualityRendering property for superior output. Control rendering speed and quality for perfect results.
type: docs
weight: 210
url: /net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.

```csharp
public bool UseHighQualityRendering { get; set; }
```

## Remarks

The default value is `false`.

This property is used when the document is exported to image formats: Tiff, Png, Bmp, Jpeg, Emf.

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
