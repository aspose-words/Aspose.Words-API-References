---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words for .NET
description: 探索 SvgSaveOptions TextOutputMode 属性，该属性可控制 SVG 中的文本渲染，从而增强视觉质量和自定义功能。立即优化您的图形！
type: docs
weight: 120
url: /zh/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

获取或设置一个值，确定文本在 SVG 中的呈现方式。

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## 评论

使用此属性来获取或设置以 SVG 格式保存时文档内文本的呈现方式 。

默认值为UseTargetMachineFonts。

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
