---
title: ImageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words for .NET
description: 调整 ImageSaveOptions 中的 JpegQuality 属性，优化 JPEG 图像质量，带来惊艳视觉效果和更佳性能。非常适合开发者！
type: docs
weight: 80
url: /zh/net/aspose.words.saving/imagesaveoptions/jpegquality/
---
## ImageSaveOptions.JpegQuality property

获取或设置确定生成的 JPEG 图像质量的值。

```csharp
public int JpegQuality { get; set; }
```

## 评论

仅当保存为 JPEG 时才有效。

使用此属性可获取或设置以 JPEG 格式保存时生成的图像的质量。 的值可以从 0 到 100 变化，其中 0 表示质量最差但压缩率最大，而 100 表示质量最好但压缩率最小。

默认值为 95。

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

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
