---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PdfZoomBehavior 枚举，实现可自定义的 PDF 缩放设置。通过自定义 PDF 文档的查看选项，提升用户体验。
type: docs
weight: 6340
url: /zh/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

指定在 PDF 查看器中打开 PDF 文档时应用的缩放类型。

```csharp
public enum PdfZoomBehavior
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 文档的显示方式取决于 PDF 查看器。通常，查看器会根据页面宽度显示文档。 |
| ZoomFactor | `1` | 使用指定的缩放比例显示页面。 |
| FitPage | `2` | 显示页面，使其完全可见。 |
| FitWidth | `3` | 适合页面宽度。 |
| FitHeight | `4` | 适合页面高度。 |
| FitBox | `5` | 适合边界框（包含页面上所有可见元素的矩形）。 |

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
