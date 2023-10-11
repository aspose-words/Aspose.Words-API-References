---
title: PdfSaveOptions.InterpolateImages
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 指示图像插值是否应由合格读取器执行的标志 当错误的指定后该标志不会写入输出文档并且 改为使用阅读器的默认行为
type: docs
weight: 210
url: /zh/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

指示图像插值是否应由合格读取器执行的标志。 当`错误的`指定后，该标志不会写入输出文档，并且 改为使用阅读器的默认行为。

```csharp
public bool InterpolateImages { get; set; }
```

### 评论

当源图像的分辨率明显低于输出设备的分辨率时， 每个源样本覆盖许多设备像素。因此，图像可能会出现锯齿状或块状。 在渲染过程中应用图像插值算法可以减少这些视觉伪影。 图像插值 尝试生成平滑的图像，而不是使用相同颜色绘制源样本覆盖的所有像素。相邻样本值之间的转换。

符合要求的读者可以选择不实现 PDF 的此功能， 或者可以使用它希望的任何特定插值实现。

默认值为`错误的`。

PDF/A 合规性禁止使用插值标志。`错误的`保存为 PDF/A 时，将自动使用值 。

### 例子

演示如何在将文档保存为 PDF 时对图像执行插值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“InterpolateImages”属性设置为“true”以使打开此文档的阅读器插入图像。
// 它们的分辨率应低于显示文档的设备的分辨率。
// 将“InterpolateImages”属性设置为“false”，以使阅读器不应用任何插值。
saveOptions.InterpolateImages = interpolateImages;

// 当我们使用 Adobe Acrobat 等阅读器打开此文档时，我们需要放大图像
// 如果我们在启用插值的情况下保存文档，则可以查看插值效果。
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

演示如何提高渲染文档中图像的质量 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“InterpolateImages”属性设置为“true”以使打开此文档的阅读器插入图像。
// 它们的分辨率应低于显示文档的设备的分辨率。
// 将“InterpolateImages”属性设置为“false”，以使阅读器不应用任何插值。
saveOptions.InterpolateImages = interpolateImages;

// 当我们使用 Adobe Acrobat 等阅读器打开此文档时，我们需要放大图像
// 如果我们在启用插值的情况下保存文档，则可以查看插值效果。
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


