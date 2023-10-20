---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.DownsampleOptions 班级. 允许指定下采样选项 在 C#.
type: docs
weight: 4970
url: /zh/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

允许指定下采样选项。

要了解更多信息，请访问[保存文档](https://docs.aspose.com/words/net/save-a-document/)文档文章。

```csharp
public class DownsampleOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [DownsampleOptions](downsampleoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | 指定是否应对图像进行下采样。 |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | 指定图像应降采样到的分辨率（以每英寸像素为单位）。 |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | 指定阈值分辨率（以每英寸像素为单位）。 如果文档中图像的分辨率小于阈值，则 将不会应用下采样算法。 值 0 表示不使用阈值检查，并且所有图像都将使用阈值检查。可以减小尺寸并进行下采样。 |

## 例子

演示如何更改 PDF 文档中图像的分辨率。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 默认情况下，Aspose.Words 将我们保存为 PDF 的文档中的所有图像缩减采样至 220 ppi。
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// 将“分辨率”属性设置为“36”，将所有图像采样到 36 ppi。
options.DownsampleOptions.Resolution = 36;

// 设置“ResolutionThreshold”属性以仅应用下采样
// 分辨率高于 128 ppi 的图像。
options.DownsampleOptions.ResolutionThreshold = 128;

// 在此阶段仅对文档中的前两个图像进行下采样。
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
