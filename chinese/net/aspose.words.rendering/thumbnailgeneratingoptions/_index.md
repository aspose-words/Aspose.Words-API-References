---
title: ThumbnailGeneratingOptions Class
linktitle: ThumbnailGeneratingOptions
articleTitle: ThumbnailGeneratingOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Rendering.ThumbnailGeneratingOptions 类，通过可定制的功能和改进的质量来增强文档缩略图生成。
type: docs
weight: 5330
url: /zh/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

可用于在生成文档缩略图时指定附加选项。

```csharp
public class ThumbnailGeneratingOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ThumbnailGeneratingOptions](thumbnailgeneratingoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | 指定是否从文档的第一页或第一幅图像生成缩略图。 |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | 生成的缩略图的大小（以像素为单位）。 默认值为 600x900。 |

## 评论

用户可以调用方法[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/)生成 [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/)用于文档。

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

* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)
