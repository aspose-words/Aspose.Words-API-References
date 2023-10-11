---
title: PdfSaveOptions.PreblendImages
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 获取或设置一个值确定是否预混合具有黑色背景颜色的透明图像
type: docs
weight: 260
url: /zh/net/aspose.words.saving/pdfsaveoptions/preblendimages/
---
## PdfSaveOptions.PreblendImages property

获取或设置一个值，确定是否预混合具有黑色背景颜色的透明图像。

```csharp
public bool PreblendImages { get; set; }
```

### 评论

预混合图像可以改善 PDF 文档在 Adobe Reader 中的视觉外观并消除抗锯齿伪影。

为了正确显示预混合图像，PDF 查看器应用程序必须支持软遮罩图像字典中的 /Matte 条目。 此外，预混合图像可能会降低 PDF 渲染性能。

默认值为`错误的`。

### 例子

演示如何在将文档保存为 PDF 时预混合具有透明背景的图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“PreblendImages”属性设置为“true”以预混合透明图像
// 有背景，这可能会减少伪影。
// 将“PreblendImages”属性设置为“false”以正常渲染透明图像。
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImages.pdf", options);
```

演示如何预混合具有透明背景的图像 (.NetStandard 2.0)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“PreblendImages”属性设置为“true”以预混合透明图像
// 有背景，这可能会减少伪影。
// 将“PreblendImages”属性设置为“false”以正常渲染透明图像。
options.PreblendImages = preblendImages;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreblendImagesNetStandard2.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


