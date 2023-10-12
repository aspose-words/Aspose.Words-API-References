---
title: DocumentProperty.ToByteArray
second_title: Aspose.Words for .NET API 参考
description: DocumentProperty 方法. 以字节数组形式返回属性值
type: docs
weight: 70
url: /zh/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

以字节数组形式返回属性值。

```csharp
public byte[] ToByteArray()
```

### 评论

如果属性类型不是，则抛出异常ByteArray。

### 例子

演示如何向保存为 Epub 的文档添加缩略图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 如果我们将一个文档保存为 Epub，其“缩略图”属性包含我们添加的图像数据，
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

* class [DocumentProperty](../)
* 命名空间 [Aspose.Words.Properties](../../documentproperty/)
* 部件 [Aspose.Words](../../../)


