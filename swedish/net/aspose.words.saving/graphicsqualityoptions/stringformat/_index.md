---
title: GraphicsQualityOptions.StringFormat
linktitle: StringFormat
articleTitle: StringFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen GraphicsQualityOptions StringFormat för förbättrad kontroll över textlayout, inklusive justering, ellips och OpenType-funktioner för bättre visning.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/graphicsqualityoptions/stringformat/
---
## GraphicsQualityOptions.StringFormat property

Hämtar eller ställer in information om textlayout (såsom justering, orientering och tabbstopp), visar manipulationer (såsom ellipsinfogning och nationell sifferersättning) och OpenType-funktioner.

```csharp
public StringFormat StringFormat { get; set; }
```

## Exempel

Visar hur man ställer in alternativ för renderingskvalitet vid konvertering av dokument till bildformat.

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

### Se även

* class [GraphicsQualityOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
