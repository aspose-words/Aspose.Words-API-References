---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: 用于 .NET 的 Aspose.Words
description: SvgSaveOptions ShowPageBorder 财产. 控制是否向页面轮廓添加边框 默认为真的 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

控制是否向页面轮廓添加边框。 默认为`真的`.

```csharp
public bool ShowPageBorder { get; set; }
```

## 例子

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

* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
