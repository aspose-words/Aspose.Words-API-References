---
title: ImageSaveOptions
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words for .NET
description: 探索 ImageSaveOptions 构造函数，将图像保存为多种格式，例如 TIFF、PNG、BMP、JPEG、EMF、EPS、WebP 和 SVG。优化您的图像处理！
type: docs
weight: 10
url: /zh/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

初始化此类的新实例，可用于保存渲染图像Tiff，Png，Bmp , Jpeg，Emf，Eps , WebP或者Svg格式.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | SaveFormat | 可以是 Tiff，Png，Bmp , Jpeg，Emf，EpsWebP或者Svg格式. |

## 例子

展示如何在将文档保存为 JPEG 时配置压缩。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// 将“JpegQuality”属性设置为“10”以在呈现文档时使用更强的压缩。
// 这将减小文档的文件大小，但图像将显示更明显的压缩伪影。
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// 将“JpegQuality”属性设置为“100”以在渲染文档时使用较弱的压缩。
// 这将提高图像的质量，但会增加文件大小。
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
