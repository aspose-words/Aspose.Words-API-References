---
title: GraphicsQualityOptions.TextRenderingHint
linktitle: TextRenderingHint
articleTitle: TextRenderingHint
second_title: Aspose.Words for .NET
description: Discover the GraphicsQualityOptions TextRenderingHint property for optimal text rendering in your graphics. Enhance visual quality and performance today!
type: docs
weight: 70
url: /net/aspose.words.saving/graphicsqualityoptions/textrenderinghint/
---
## GraphicsQualityOptions.TextRenderingHint property

Gets or sets the rendering mode for text associated with this Graphics.

```csharp
public TextRenderingHint? TextRenderingHint { get; set; }
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
