---
title: ImageSaveOptions.GraphicsQualityOptions
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words for .NET
description: 使用 ImageSaveOptions GraphicsQualityOptions 属性优化您的图形，实现精确的渲染模式和卓越的品质，获得令人惊叹的视觉效果。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/imagesaveoptions/graphicsqualityoptions/
---
## ImageSaveOptions.GraphicsQualityOptions property

允许指定渲染模式和质量Graphics对象.

```csharp
public GraphicsQualityOptions GraphicsQualityOptions { get; set; }
```

## 评论

使用此属性可以覆盖 Aspose.Words 引擎默认提供的图形设置。

仅当将文档保存为类似图像的格式时它才会生效。

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

* class [GraphicsQualityOptions](../../graphicsqualityoptions/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
