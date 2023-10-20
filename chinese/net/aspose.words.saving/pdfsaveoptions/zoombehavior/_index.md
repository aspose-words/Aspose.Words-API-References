---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions ZoomBehavior 财产. 获取或设置一个值该值确定使用 PDF 查看器打开文档时应应用的缩放类型 在 C#.
type: docs
weight: 320
url: /zh/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

获取或设置一个值，该值确定使用 PDF 查看器打开文档时应应用的缩放类型。

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## 评论

默认值为None ，即没有应用拟合。

## 例子

显示如何设置阅读器在打开呈现的 PDF 文档时应用的默认缩放。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
// 将“ZoomBehavior”属性设置为“PdfZoomBehavior.ZoomFactor”以获取 PDF 阅读器
// 当我们打开文档时应用基于百分比的缩放因子。
// 将“ZoomFactor”属性设置为“25”，将缩放因子的值设为 25%。
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// 当我们使用 Adobe Acrobat 等阅读器打开此文档时，我们将看到文档按实际大小的 1/4 缩放。
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### 也可以看看

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
