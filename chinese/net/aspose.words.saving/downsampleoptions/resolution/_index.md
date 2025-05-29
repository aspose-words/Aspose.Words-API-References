---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words for .NET
description: 使用 DownsampleOptions Resolution 属性优化图像质量，定义理想的每英寸像素数以获得卓越的下采样结果。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

指定图像应下采样到的分辨率（以每英寸像素为单位）。

```csharp
public int Resolution { get; set; }
```

## 评论

默认值为 220 ppi。

## 例子

展示如何更改 PDF 文档中图像的分辨率。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 默认情况下，Aspose.Words 将我们保存为 PDF 的文档中的所有图像下采样至 220 ppi。
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// 将“分辨率”属性设置为“36”，以将所有图像下采样到 36 ppi。
options.DownsampleOptions.Resolution = 36;

// 设置“ResolutionThreshold”属性，仅将下采样应用于
// 分辨率高于 128 ppi 的图像。
options.DownsampleOptions.ResolutionThreshold = 128;

// 在此阶段，仅对文档中的前两幅图像进行下采样。
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### 也可以看看

* class [DownsampleOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
