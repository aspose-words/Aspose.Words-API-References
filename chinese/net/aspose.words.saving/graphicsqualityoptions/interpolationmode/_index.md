---
title: GraphicsQualityOptions.InterpolationMode
linktitle: InterpolationMode
articleTitle: InterpolationMode
second_title: Aspose.Words for .NET
description: 探索 GraphicsQualityOptions InterpolationMode 属性，轻松自定义图形的插值设置，以增强视觉质量。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/graphicsqualityoptions/interpolationmode/
---
## GraphicsQualityOptions.InterpolationMode property

获取或设置与此 Graphics 相关的插值模式。

```csharp
public InterpolationMode? InterpolationMode { get; set; }
```

## 例子

展示如何在将文档转换为图像格式时设置渲染质量选项。

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

### 也可以看看

* class [GraphicsQualityOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
