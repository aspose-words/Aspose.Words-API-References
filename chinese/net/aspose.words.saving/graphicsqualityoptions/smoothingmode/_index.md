---
title: GraphicsQualityOptions.SmoothingMode
second_title: Aspose.Words for .NET API 参考
description: GraphicsQualityOptions 财产. 获取或设置此 Graphics 的渲染质量
type: docs
weight: 50
url: /zh/net/aspose.words.saving/graphicsqualityoptions/smoothingmode/
---
## GraphicsQualityOptions.SmoothingMode property

获取或设置此 Graphics 的渲染质量。

```csharp
public SmoothingMode? SmoothingMode { get; set; }
```

### 例子

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
* 命名空间 [Aspose.Words.Saving](../../graphicsqualityoptions/)
* 部件 [Aspose.Words](../../../)


