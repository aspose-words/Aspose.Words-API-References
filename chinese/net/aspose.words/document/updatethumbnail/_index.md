---
title: Document.UpdateThumbnail
second_title: Aspose.Words for .NET API 参考
description: Document 方法. 更新Thumbnail根据指定选项的文档
type: docs
weight: 800
url: /zh/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(ThumbnailGeneratingOptions) {#updatethumbnail_1}

更新[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/)根据指定选项的文档。

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | 要使用的生成选项。 |

### 评论

的[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/)允许您指定缩略图的来源、大小和其他选项。 如果尝试生成缩略图失败，则不更改。

### 例子

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

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

更新[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/)使用默认选项的文档。

```csharp
public void UpdateThumbnail()
```

### 例子

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

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


