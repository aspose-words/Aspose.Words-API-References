---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: Aspose.Words for .NET
description: 探索 SvgSaveOptions 的 ShowPageBorder 属性，自定义页面轮廓。轻松控制边框——默认设置为 true，方便使用！
type: docs
weight: 110
url: /zh/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

控制是否在页面轮廓上添加边框。 默认值为`真的`.

```csharp
public bool ShowPageBorder { get; set; }
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
