---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words for .NET
description: 使用 BuiltInDocumentProperties 管理文档的视觉效果。轻松获取或设置缩略图，增强文档的呈现效果和组织性。
type: docs
weight: 310
url: /zh/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

获取或设置文档的缩略图。

```csharp
public byte[] Thumbnail { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| InvalidOperationException | 如果图像无效或其格式不支持特定格式的文档，则抛出此异常。 |

## 评论

目前，此属性仅在将文档导出为 ePub 时使用， 它不能从其他文档格式读取或写入。

可以将任意格式的图像设置为此属性，但在导出时会检查格式。

只有 gif、jpeg 和 png 图像可用于 ePub 出版。

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
