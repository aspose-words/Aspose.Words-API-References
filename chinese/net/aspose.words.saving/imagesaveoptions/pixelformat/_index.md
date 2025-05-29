---
title: ImageSaveOptions.PixelFormat
linktitle: PixelFormat
articleTitle: PixelFormat
second_title: Aspose.Words for .NET
description: 探索 ImageSaveOptions PixelFormat 属性，轻松自定义生成图像的像素格式，以获得最佳质量和性能。
type: docs
weight: 120
url: /zh/net/aspose.words.saving/imagesaveoptions/pixelformat/
---
## ImageSaveOptions.PixelFormat property

获取或设置生成图像的像素格式。

```csharp
public ImagePixelFormat PixelFormat { get; set; }
```

## 评论

此属性仅在保存为光栅图像格式时有效。

默认值为Format32BppArgb。

由于 GDI+ 的工作，输出图像的像素格式可能与设置的值 不同。

## 例子

展示如何选择将文档渲染为图像的每像素位数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 当我们将文档保存为图像时，我们可以将 SaveOptions 对象传递给
// 为保存操作将生成的图像选择像素格式。
// 不同的每像素比特率将影响生成图像的质量和文件大小。
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// 我们可以克隆 ImageSaveOptions 实例。
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### 也可以看看

* enum [ImagePixelFormat](../../imagepixelformat/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
