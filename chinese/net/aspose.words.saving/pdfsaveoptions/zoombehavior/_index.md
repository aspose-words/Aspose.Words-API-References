---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions ZoomBehavior，控制缩放设置，以便在 PDF 查看器中获得最佳观看效果。通过定制文档显示，提升用户体验！
type: docs
weight: 350
url: /zh/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

获取或设置一个值，该值确定使用 PDF 查看器打开文档时应应用哪种类型的缩放。

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## 评论

默认值为None ，即不适用。

## 例子

展示如何设置阅读器打开渲染的 PDF 文档时应用的默认缩放。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
// 将“ZoomBehavior”属性设置为“PdfZoomBehavior.ZoomFactor”，以使 PDF 阅读器
// 当我们用它打开文档时应用基于百分比的缩放因子。
// 将“ZoomFactor”属性设置为“25”，使缩放系数的值为 25%。
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// 当我们使用 Adobe Acrobat 等阅读器打开此文档时，我们将看到该文档缩放至其实际大小的 1/4。
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### 也可以看看

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
