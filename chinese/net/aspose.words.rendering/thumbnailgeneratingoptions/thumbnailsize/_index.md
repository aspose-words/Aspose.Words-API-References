---
title: ThumbnailGeneratingOptions.ThumbnailSize
linktitle: ThumbnailSize
articleTitle: ThumbnailSize
second_title: Aspose.Words for .NET
description: 使用我们的 ThumbnailSize 属性探索可自定义的缩略图选项。生成完美像素大小的缩略图，默认分辨率为 600x900，以获得最佳显示效果！
type: docs
weight: 30
url: /zh/net/aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/
---
## ThumbnailGeneratingOptions.ThumbnailSize property

生成的缩略图的大小（以像素为单位）。 默认值为 600x900。

```csharp
public Size ThumbnailSize { get; set; }
```

## 例子

显示如何更新文档的缩略图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 将文档保存为 .epub 时，有两种设置缩略图的方法。
// 1 - 使用文档的第一页：
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - 使用在文档中找到的第一张图片：
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### 也可以看看

* class [ThumbnailGeneratingOptions](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)
