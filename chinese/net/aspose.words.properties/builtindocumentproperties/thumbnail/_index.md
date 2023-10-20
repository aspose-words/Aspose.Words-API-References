---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: 用于 .NET 的 Aspose.Words
description: BuiltInDocumentProperties Thumbnail 财产. 获取或设置文档的缩略图 在 C#.
type: docs
weight: 280
url: /zh/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

获取或设置文档的缩略图。

```csharp
public byte[] Thumbnail { get; set; }
```

## 评论

目前，此属性仅在将文档导出到 ePub 时使用， 它不会从其他文档格式读取和写入。

该属性可以设置任意格式的图片，但导出时会检查格式。 InvalidOperationException如果图像无效或其格式不支持 特定格式的文档，则抛出此错误。

只有 gif、jpeg 和 png 图像可用于 ePub 发布。

## 例子

展示如何将缩略图添加到我们保存为 Epub 的文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 如果我们保存一个文档，其“缩略图”属性包含我们添加的图像数据，作为 Epub，
// 打开该文档的阅读器可能会在第一页之前显示图像。
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// 我们可以提取文档的缩略图并将其保存到本地文件系统。
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
