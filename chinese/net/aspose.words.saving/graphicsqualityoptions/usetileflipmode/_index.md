---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words for .NET
description: 探索 GraphicsQualityOptions UseTileFlipMode 属性来控制 WrapMode 设置，从而增强应用程序的视觉质量。
type: docs
weight: 80
url: /zh/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

获取或设置一个标志，指示 WrapMode 是否为 TileFlipXY。

```csharp
public bool UseTileFlipMode { get; set; }
```

## 评论

这WrapMode指定当纹理或渐变小于被填充的区域时如何平铺。

默认使用Tile（指定平铺而不翻转）。 这会导致缩放图像（高分辨率）的渲染不准确。

此属性允许将 WrapMode 切换为TileFlipXY（指定当您沿行移动时，图块会水平翻转 ，当您沿列移动时，图块会垂直翻转）。

## 例子

展示如何防止高分辨率渲染时出现白线。

```csharp
Document doc = new Document(MyDir + "Shape high dpi.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShapeRenderer renderer = shape.GetShapeRenderer();

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png)
{
    Resolution = 500, GraphicsQualityOptions = new GraphicsQualityOptions { UseTileFlipMode = true }
};
renderer.Save(ArtifactsDir + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
```

### 也可以看看

* class [GraphicsQualityOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
