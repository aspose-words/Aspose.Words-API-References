---
title: SvgSaveOptions.FitToViewPort
second_title: Aspose.Words for .NET API 参考
description: SvgSaveOptions 财产. 指定输出 SVG 是否应填充可用视口区域浏览器窗口或容器 当设置为 true 时输出 SVG 的宽度和高度设置为 100
type: docs
weight: 30
url: /zh/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

指定输出 SVG 是否应填充可用视口区域（浏览器窗口或容器）。 当设置为 true 时，输出 SVG 的宽度和高度设置为 100%。

默认值为假。

```csharp
public bool FitToViewPort { get; set; }
```

### 例子

演示如何在将 .docx 文档转换为 .svg 时模拟图像的属性。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 将 SvgSaveOptions 对象配置为没有页面边框或可选文本的保存。
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
* 命名空间 [Aspose.Words.Saving](../../svgsaveoptions/)
* 部件 [Aspose.Words](../../../)


