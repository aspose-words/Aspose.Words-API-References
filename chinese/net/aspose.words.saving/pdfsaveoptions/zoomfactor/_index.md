---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions ZoomFactor 财产. 获取或设置确定文档缩放系数以百分比表示的值 在 C#.
type: docs
weight: 330
url: /zh/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

获取或设置确定文档缩放系数（以百分比表示）的值。

```csharp
public int ZoomFactor { get; set; }
```

## 评论

仅当以下情况时才使用该值[`ZoomBehavior`](../zoombehavior/)被设定为ZoomFactor.

## 例子

演示如何设置读者在打开渲染的 PDF 文档时应用的默认缩放。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
// 将“ZoomBehavior”属性设置为“PdfZoomBehavior.ZoomFactor”以使 PDF 阅读器能够
// 当我们用它打开文档时应用基于百分比的缩放因子。
// 将“ZoomFactor”属性设置为“25”，为缩放系数指定 25% 的值。
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// 当我们使用 Adobe Acrobat 等阅读器打开此文档时，我们将看到文档缩放为其实际大小的 1/4。
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
