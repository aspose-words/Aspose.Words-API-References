---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words for .NET
description: 了解 SvgSaveOptions FitToViewPort 属性如何优化您的 SVG 输出，以完美填充任何浏览器窗口或容器，从而获得令人惊叹的视觉效果。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

指定输出 SVG 是否应填充可用的视口区域（浏览器窗口或容器）。 设置为`真的`输出 SVG 的宽度和高度设置为 100%。

默认值为`错误的`。

```csharp
public bool FitToViewPort { get; set; }
```

## 例子

展示如何在将 .docx 文档转换为 .svg 时模仿图像的属性。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 配置 SvgSaveOptions 对象以保存无页面边框或可选文本。
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### 也可以看看

* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
