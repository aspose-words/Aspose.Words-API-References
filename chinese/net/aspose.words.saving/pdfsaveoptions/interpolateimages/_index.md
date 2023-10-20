---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: 用于 .NET 的 Aspose.Words
description: PdfSaveOptions InterpolateImages 财产. 指示图像插值是否应由合格阅读器执行的标志 当错误的指定时标志不会写入输出文档 会使用 reader 的默认行为 在 C#.
type: docs
weight: 210
url: /zh/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

指示图像插值是否应由合格阅读器执行的标志。 当`错误的`指定时，标志不会写入输出文档， 会使用 reader 的默认行为。

```csharp
public bool InterpolateImages { get; set; }
```

## 评论

当源图像的分辨率明显低于输出设备的分辨率时， 每个源样本覆盖了许多设备像素。因此，图像可能会出现锯齿状或块状。 可以通过在渲染期间应用图像插值算法来减少这些视觉伪影。 不是用相同颜色绘制源样本覆盖的所有像素，而是图像插值 尝试产生平滑相邻样本值之间的转换。

符合要求的阅读器可以选择不实现 PDF 的此功能， 或可以使用它希望的任何特定插值实现。

默认值为`错误的`.

PDF/A 合规性禁止插值标志。`错误的`保存到 PDF/A 时将自动使用值 。

## 例子

显示如何在将文档保存为 PDF 时对图像执行插值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“InterpolateImages”属性设置为“true”，让打开此文档的阅读器插入图像。
// 它们的分辨率应该低于显示文档的设备的分辨率。
// 将“InterpolateImages”属性设置为“false”以使阅读器不应用任何插值。
saveOptions.InterpolateImages = interpolateImages;

// 当我们使用 Adobe Acrobat 等阅读器打开此文档时，我们需要放大图像
// 如果我们在启用它的情况下保存文档，则查看插值效果。
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

展示如何提高渲染文档 (.NetStandard 2.0) 中图像的质量。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“InterpolateImages”属性设置为“true”，让打开此文档的阅读器插入图像。
// 它们的分辨率应该低于显示文档的设备的分辨率。
// 将“InterpolateImages”属性设置为“false”以使阅读器不应用任何插值。
saveOptions.InterpolateImages = interpolateImages;

// 当我们使用 Adobe Acrobat 等阅读器打开此文档时，我们需要放大图像
// 如果我们在启用它的情况下保存文档，则查看插值效果。
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
