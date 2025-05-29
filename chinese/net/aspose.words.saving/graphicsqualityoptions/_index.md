---
title: GraphicsQualityOptions Class
linktitle: GraphicsQualityOptions
articleTitle: GraphicsQualityOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.GraphicsQualityOptions 类，通过可自定义的选项来增强文档图形质量，从而获得卓越的输出。
type: docs
weight: 5790
url: /zh/net/aspose.words.saving/graphicsqualityoptions/
---
## GraphicsQualityOptions class

允许指定额外的Graphics质量选项。

要了解更多信息，请访问[保存文档](https://docs.aspose.com/words/net/save-a-document/)文档文章。

```csharp
public class GraphicsQualityOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [GraphicsQualityOptions](graphicsqualityoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CompositingMode](../../aspose.words.saving/graphicsqualityoptions/compositingmode/) { get; set; } | 获取或设置一个值，该值指定如何将合成图像绘制到此 Graphics。 |
| [CompositingQuality](../../aspose.words.saving/graphicsqualityoptions/compositingquality/) { get; set; } | 获取或设置绘制到此 Graphics 的合成图像的渲染质量。 |
| [InterpolationMode](../../aspose.words.saving/graphicsqualityoptions/interpolationmode/) { get; set; } | 获取或设置与此 Graphics 相关的插值模式。 |
| [SmoothingMode](../../aspose.words.saving/graphicsqualityoptions/smoothingmode/) { get; set; } | 获取或设置此 Graphics 的渲染质量。 |
| [StringFormat](../../aspose.words.saving/graphicsqualityoptions/stringformat/) { get; set; } | 获取或设置文本布局信息（例如对齐方式、方向和制表位）显示操作 （例如省略号插入和国家数字替换）和 OpenType 功能。 |
| [TextRenderingHint](../../aspose.words.saving/graphicsqualityoptions/textrenderinghint/) { get; set; } | 获取或设置与此 Graphics 关联的文本的渲染模式。 |
| [UseTileFlipMode](../../aspose.words.saving/graphicsqualityoptions/usetileflipmode/) { get; set; } | 获取或设置一个标志，指示 WrapMode 是否为 TileFlipXY。 |

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
