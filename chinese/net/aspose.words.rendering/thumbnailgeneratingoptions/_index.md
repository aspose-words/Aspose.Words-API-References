---
title: ThumbnailGeneratingOptions Class
linktitle: ThumbnailGeneratingOptions
articleTitle: ThumbnailGeneratingOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Rendering.ThumbnailGeneratingOptions 班级. 可用于在生成文档缩略图时指定其他选项 在 C#.
type: docs
weight: 4600
url: /zh/net/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class

可用于在生成文档缩略图时指定其他选项。

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
| [GenerateFromFirstPage](../../aspose.words.rendering/thumbnailgeneratingoptions/generatefromfirstpage/) { get; set; } | 指定是否从文档的第一页或第一张图像生成缩略图。 |
| [ThumbnailSize](../../aspose.words.rendering/thumbnailgeneratingoptions/thumbnailsize/) { get; set; } | 生成的缩略图的大小（以像素为单位）。 默认值为 600x900。 |

## 评论

用户可以调用方法[`UpdateThumbnail`](../../aspose.words/document/updatethumbnail/)生成 [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/)对于文档.

## 例子

展示如何更新文档的缩略图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// 将文档保存到 .epub 时有两种设置缩略图的方法。
// 1 - 使用文档的第一页：
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - 使用文档中找到的第一张图像：
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### 也可以看看

* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)
