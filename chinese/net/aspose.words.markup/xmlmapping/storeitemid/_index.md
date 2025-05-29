---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: Aspose.Words for .NET
description: 探索 XmlMapping StoreItemId 属性，用于自定义 XML 数据标识符。使用我们独特的解决方案增强 XPath 评估，实现高效的数据管理。
type: docs
weight: 40
url: /zh/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

指定自定义 XML 数据部分的自定义 XML 数据标识符，该标识符应用于评估[`XPath`](../xpath/)表达式.

```csharp
public string StoreItemId { get; }
```

## 例子

展示如何获取 XML 部分的自定义 XML 数据标识符。

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// 结构化文档标签具有 GUID 形式的 ID。
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### 也可以看看

* class [XmlMapping](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
