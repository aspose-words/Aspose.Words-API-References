---
title: FixedPageSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words for .NET
description: 使用 FixedPageSaveOptions 优化 HTML 文档中的 JPEG 质量。轻松调整 JpegQuality 属性，获得令人惊叹的图像清晰度。
type: docs
weight: 20
url: /zh/net/aspose.words.saving/fixedpagesaveoptions/jpegquality/
---
## FixedPageSaveOptions.JpegQuality property

获取或设置确定 Html 文档中 JPEG 图像质量的值。

```csharp
public int JpegQuality { get; set; }
```

## 评论

仅当文档包含 JPEG 图像时才有效。

使用此属性可以获取或设置以固定页面格式保存文档时图像的质量。 的值可以从 0 到 100 变化，其中 0 表示质量最差但压缩率最大，而 100 表示质量最好但压缩率最小。

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

* class [FixedPageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
