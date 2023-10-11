---
title: ImageSaveOptions.ImageSaveOptions
second_title: Aspose.Words for .NET API 参考
description: ImageSaveOptions 构造函数. 初始化此类的一个新实例可用于将渲染图像保存在 中TiffPngBmp JpegEmfEps 或Svg格式.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

初始化此类的一个新实例，可用于将渲染图像保存在 中Tiff,Png,Bmp, Jpeg,Emf,Eps 或Svg格式.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | SaveFormat | 可以是 Tiff,Png,Bmp, Jpeg,Emf,Eps 或Svg格式. |

### 例子

演示如何在将文档另存为 JPEG 时配置压缩。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// 将“JpegQuality”属性设置为“10”，以便在渲染文档时使用更强的压缩。
// 这将减小文档的文件大小，但图像将显示更突出的压缩伪影。
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// 将“JpegQuality”属性设置为“100”，以便在渲染文档时使用较弱的压缩。
// 这将以增加文件大小为代价提高图像质量。
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../imagesaveoptions/)
* 部件 [Aspose.Words](../../../)


