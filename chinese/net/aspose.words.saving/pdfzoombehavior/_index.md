---
title: Enum PdfZoomBehavior
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.PdfZoomBehavior 枚举. 指定在 PDF 查看器中打开 PDF 文档时应用于该文档的缩放类型
type: docs
weight: 5540
url: /zh/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

指定在 PDF 查看器中打开 PDF 文档时应用于该文档的缩放类型。

```csharp
public enum PdfZoomBehavior
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 文档如何显示由 PDF 查看器决定。通常，查看器会显示文档以适合页面宽度。 |
| ZoomFactor | `1` | 使用指定的缩放系数显示页面。 |
| FitPage | `2` | 显示页面，使其完全可见。 |
| FitWidth | `3` | 适合页面宽度。 |
| FitHeight | `4` | 适合页面的高度。 |
| FitBox | `5` | 适合边界框（包含页面上所有可见元素的矩形）。 |

### 例子

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


