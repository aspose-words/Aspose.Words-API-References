---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: 用于 .NET 的 Aspose.Words
description: SaveOutputParameters ContentType 财产. 返回标识已保存文档类型的 ContentType 字符串Internet 媒体类型 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

返回标识已保存文档类型的 Content-Type 字符串（Internet 媒体类型）。

```csharp
public string ContentType { get; }
```

## 例子

演示如何访问文档保存操作的输出参数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 保存文档后，我们可以访问新创建的输出文档的 Internet Media Type（MIME 类型）。
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// 该属性根据保存格式而变化。
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### 也可以看看

* class [SaveOutputParameters](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
