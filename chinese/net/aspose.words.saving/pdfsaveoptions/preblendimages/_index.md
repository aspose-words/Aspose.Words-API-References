---
title: PdfSaveOptions.PreblendImages
linktitle: PreblendImages
articleTitle: PreblendImages
second_title: Aspose.Words for .NET
description: 探索 PdfSaveOptions 的 PreblendImages 属性。轻松控制透明图像混合，提升文档质量和视觉吸引力。
type: docs
weight: 270
url: /zh/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

获取或设置一个值，确定是否将透明图像与黑色背景颜色预混合。

```csharp
public bool PreblendImages { get; set; }
```

## 评论

预混合图像可能会改善 PDF 文档在 Adobe Reader 中的视觉外观并消除抗锯齿伪影。

为了正确显示预混合图像，PDF 查看器应用程序必须支持软蒙版图像字典中的 /Matte 条目。 此外，预混合图像可能会降低 PDF 渲染性能。

默认值为`错误的`。

## 例子

展示如何在将文档保存为 PDF 时将图像与透明背景预混合。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();
// 将“PreblendImages”属性设置为“true”以预混合透明图像
// 带有背景，这可能会减少伪影。
// 将“PreblendImages”属性设置为“false”以正常渲染透明图像。
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
