---
title: ThumbnailGeneratingOptions.GenerateFromFirstPage
linktitle: GenerateFromFirstPage
articleTitle: GenerateFromFirstPage
second_title: Aspose.Words for .NET
description: 了解 GenerateFromFirstPage 选项如何从文档的第一页或图像创建缩略图，轻松增强您的视觉内容。
type: docs
weight: 20
url: /zh/net/aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/
---
## ThumbnailGeneratingOptions.GenerateFromFirstPage property

指定是否从文档的第一页或第一幅图像生成缩略图。

```csharp
public bool GenerateFromFirstPage { get; set; }
```

## 评论

默认为`真的`，这意味着缩略图将从文档的第一页生成。 如果值为`错误的`并且文档中没有图像，缩略图将从文档第一页生成 。

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
