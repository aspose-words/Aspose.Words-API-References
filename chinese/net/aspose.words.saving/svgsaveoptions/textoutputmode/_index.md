---
title: SvgSaveOptions.TextOutputMode
second_title: Aspose.Words for .NET API 参考
description: SvgSaveOptions 财产. 获取或设置一个值确定如何在 SVG 中呈现文本
type: docs
weight: 90
url: /zh/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

获取或设置一个值，确定如何在 SVG 中呈现文本。

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

### 评论

使用此属性可获取或设置以 SVG 格式保存时文档内文本的渲染方式 。

默认值为UseTargetMachineFonts。

### 例子

演示如何在将 .docx 文档转换为 .svg 时模仿图像的属性。

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
* 命名空间 [Aspose.Words.Saving](../../svgsaveoptions/)
* 部件 [Aspose.Words](../../../)


