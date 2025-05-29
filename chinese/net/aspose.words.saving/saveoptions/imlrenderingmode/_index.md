---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words for .NET
description: 了解 SaveOptions ImlRenderingMode 属性如何增强 InkML 对象渲染。优化您的墨迹渲染，获得更佳的视觉效果！
type: docs
weight: 90
url: /zh/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

获取或设置一个值，该值确定如何呈现墨水（InkML）对象。

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## 评论

默认值为InkML.

当文档导出为固定页面格式时使用此属性。

## 例子

展示如何渲染 Ink 对象。

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// 设置“ImlRenderingMode.InkML”忽略墨水（InkML）对象的后备形状并呈现 InkML 本身。
// 如果渲染结果不令人满意，
// 请使用“ImlRenderingMode.Fallback”来获得与以前版本类似的结果。
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### 也可以看看

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
