---
title: BuiltInDocumentProperties.SharedDocument
linktitle: SharedDocument
articleTitle: SharedDocument
second_title: Aspose.Words for .NET
description: 探索 BuiltInDocumentProperties SharedDocument 功能，它可以显示您的文档是否共享，从而增强协作和可访问性。
type: docs
weight: 280
url: /zh/net/aspose.words.properties/builtindocumentproperties/shareddocument/
---
## BuiltInDocumentProperties.SharedDocument property

表示该文档是否为共享文档。

```csharp
public bool SharedDocument { get; }
```

## 评论

Aspose.Words 不会更新此属性。

## 例子

展示如何获取扩展属性。

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
