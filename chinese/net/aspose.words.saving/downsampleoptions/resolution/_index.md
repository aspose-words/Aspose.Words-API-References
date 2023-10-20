---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: 用于 .NET 的 Aspose.Words
description: DownsampleOptions Resolution 财产. 指定图像应该被下采样到的分辨率以每英寸像素为单位 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

指定图像应该被下采样到的分辨率（以每英寸像素为单位）。

```csharp
public int Resolution { get; set; }
```

## 评论

默认值为 220 ppi。

## 例子

显示如何更改 PDF 文档中图像的分辨率。

```csharp
Document doc = new Document(MyDir + "Images.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 默认情况下，Aspose.Words 将我们保存为 PDF 的文档中的所有图像下采样到 220 ppi。
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// 将“分辨率”属性设置为“36”以将所有图像下采样到 36 ppi。
options.DownsampleOptions.Resolution = 36;

// 将“ResolutionThreshold”属性设置为仅应用下采样
// 分辨率高于 128 ppi 的图像。
options.DownsampleOptions.ResolutionThreshold = 128;

// 在这个阶段，只有文档中的前两个图像会被下采样。
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### 也可以看看

* class [DownsampleOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
