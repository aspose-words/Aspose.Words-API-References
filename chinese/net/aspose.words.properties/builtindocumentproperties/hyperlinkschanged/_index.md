---
title: BuiltInDocumentProperties.HyperlinksChanged
linktitle: HyperlinksChanged
articleTitle: HyperlinksChanged
second_title: Aspose.Words for .NET
description: 发现 BuiltInDocumentProperties HyperlinksChanged 属性，该属性可跟踪文档中超链接的更改，以增强编辑控制。
type: docs
weight: 130
url: /zh/net/aspose.words.properties/builtindocumentproperties/hyperlinkschanged/
---
## BuiltInDocumentProperties.HyperlinksChanged property

表示文档中的超链接是否已更改。

```csharp
public bool HyperlinksChanged { get; }
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
