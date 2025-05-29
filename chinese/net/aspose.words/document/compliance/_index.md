---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words for .NET
description: 轻松确保您的 OOXML 文档符合合规性标准。我们的工具会分析内容以验证 OOXML 合规性，从而增强文档的完整性。
type: docs
weight: 70
url: /zh/net/aspose.words/document/compliance/
---
## Document.Compliance property

获取根据加载的文档内容确定的 OOXML 合规版本。 仅对 OOXML 文档有意义。

```csharp
public OoxmlCompliance Compliance { get; }
```

## 评论

如果您创建了一个新的空白文档或加载非 OOXML document 返回Ecma376_2006价值。

## 例子

展示如何读取已加载文档的 Open Office XML 兼容版本。

```csharp
// 使用不同版本的 Microsoft Word 创建的文档的合规版本有所不同。
Document doc = new Document(MyDir + "Document.doc");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### 也可以看看

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
