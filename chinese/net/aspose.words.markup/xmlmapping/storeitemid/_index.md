---
title: StoreItemId
second_title: Aspose.Words for .NET API 参考
description: 为自定义 XML 数据部分指定自定义 XML 数据标识符 将用于评估XPathaspose.words.markup/xmlmapping/xpath表达式.
type: docs
weight: 40
url: /zh/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

为自定义 XML 数据部分指定自定义 XML 数据标识符， 将用于评估[`XPath`](../xpath)表达式.

```csharp
public string StoreItemId { get; }
```

### 例子

显示如何获取 XML 部件的自定义 XML 数据标识符。

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// 结构化文档标签具有 GUID 形式的 ID。
StructuredDocumentTag tag = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### 也可以看看

* class [XmlMapping](../../xmlmapping)
* 命名空间 [Aspose.Words.Markup](../../xmlmapping)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->