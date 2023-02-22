---
title: GraphicsQualityOptions.CompositingMode
second_title: Aspose.Words for .NET API 参考
description: GraphicsQualityOptions 财产. 获取或设置一个值该值指定如何将合成图像绘制到此 Graphics
type: docs
weight: 20
url: /zh/net/aspose.words.saving/graphicsqualityoptions/compositingmode/
---
## GraphicsQualityOptions.CompositingMode property

获取或设置一个值，该值指定如何将合成图像绘制到此 Graphics。

```csharp
public CompositingMode? CompositingMode { get; set; }
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


