---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions 的 InterpolateImages 属性，这是一项可提升文档图像质量的关键功能。轻松优化您的 PDF！
type: docs
weight: 210
url: /zh/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

一个标志，指示是否应由符合要求的阅读器执行图像插值。 当`错误的`指定后，标志不会写入输出文档，而是使用读取器的默认行为。

```csharp
public bool InterpolateImages { get; set; }
```

## 评论

当源图像的分辨率明显低于输出设备的分辨率时， 每个源样本会覆盖许多设备像素。因此，图像可能会出现锯齿状或块状。 可以通过在渲染过程中应用图像插值算法来减少这些视觉伪影。 图像插值并非用相同的颜色绘制源样本覆盖的所有像素，而是尝试在相邻的样本值之间产生平滑的过渡。

符合标准的阅读器可以选择不实现 PDF 的此功能， 或者可以使用其希望的任何特定插值实现。

默认值为`错误的`。

PDF/A 合规性禁止使用插值标志。`错误的`保存为 PDF/A 时将自动使用 值。

## 例子

展示如何在将文档保存为 PDF 时对图像执行插值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();
// 将“InterpolateImages”属性设置为“true”，以使打开此文档的阅读器插入图像。
// 它们的分辨率应该低于显示文档的设备的分辨率。
// 将“InterpolateImages”属性设置为“false”，以使读取器不应用任何插值。
saveOptions.InterpolateImages = interpolateImages;

// 当我们使用 Adobe Acrobat 等阅读器打开此文档时，我们需要放大图像
// 如果我们在启用该功能的情况下保存文档，则可以看到插值效果。
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
