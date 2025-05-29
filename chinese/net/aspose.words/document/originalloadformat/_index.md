---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words for .NET
description: 发现 OriginalLoadFormat 属性可以轻松访问加载到对象中的原始文档的格式，增强文档管理。
type: docs
weight: 310
url: /zh/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

获取加载到此对象的原始文档的格式。

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## 评论

如果您创建了一个新的空白文档，则返回Doc价值。

## 例子

展示如何检索文档加载操作的详细信息。

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### 也可以看看

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
