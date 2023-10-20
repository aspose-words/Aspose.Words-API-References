---
title: XmlMapping.StoreItemId
linktitle: StoreItemId
articleTitle: StoreItemId
second_title: 用于 .NET 的 Aspose.Words
description: XmlMapping StoreItemId 财产. 指定自定义 XML 数据部分的自定义 XML 数据标识符其中 应用于评估XPath表达式 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

指定自定义 XML 数据部分的自定义 XML 数据标识符，其中 应用于评估[`XPath`](../xpath/)表达式.

```csharp
public string StoreItemId { get; }
```

## 例子

演示如何获取 XML 部件的自定义 XML 数据标识符。

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// 结构化文档标签具有 GUID 形式的 ID。
StructuredDocumentTag tag = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### 也可以看看

* class [XmlMapping](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
