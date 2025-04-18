---
title: GraphicsQualityOptions.CompositingMode
linktitle: CompositingMode
articleTitle: CompositingMode
second_title: Aspose.Words for .NET
description: Discover the GraphicsQualityOptions CompositingMode property to optimize how images are rendered, enhancing your graphics performance and quality.
type: docs
weight: 20
url: /net/aspose.words.saving/graphicsqualityoptions/compositingmode/
---
## GraphicsQualityOptions.CompositingMode property

Gets or sets a value that specifies how composited images are drawn to this Graphics.

```csharp
public CompositingMode? CompositingMode { get; set; }
```

## Examples

Shows how to set render quality options while converting documents to image formats.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### See Also

* class [GraphicsQualityOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
