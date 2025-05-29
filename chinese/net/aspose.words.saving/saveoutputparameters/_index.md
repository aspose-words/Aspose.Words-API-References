---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.SaveOutputParameters 类，它提供文档保存后的重要细节，增强您的文档管理体验。
type: docs
weight: 6390
url: /zh/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

文档保存后，此对象返回给调用者，其中包含在保存操作期间生成或计算的附加信息。调用者可以使用或忽略此对象。

要了解更多信息，请访问[保存文档](https://docs.aspose.com/words/net/save-a-document/)文档文章。

```csharp
public class SaveOutputParameters
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | 返回标识已保存文档类型的 Content-Type 字符串（Internet 媒体类型）。 |

## 例子

展示如何访问文档保存操作的输出参数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 保存文档后，我们可以访问新创建的输出文档的 Internet 媒体类型（MIME 类型）。
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// 此属性根据保存格式而变化。
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
