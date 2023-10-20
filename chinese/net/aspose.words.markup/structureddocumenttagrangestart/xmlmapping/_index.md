---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTagRangeStart XmlMapping 财产. 获取一个对象该对象表示此结构化文档标记范围到当前文档的自定义 XML 部分中的 XML 数据 的映射 在 C#.
type: docs
weight: 180
url: /zh/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

获取一个对象，该对象表示此结构化文档标记范围到当前文档的自定义 XML 部分中的 XML 数据 的映射。

```csharp
public XmlMapping XmlMapping { get; }
```

## 评论

你可以使用[`SetMapping`](../../xmlmapping/setmapping/)this 对象的方法将结构化文档标记范围映射到 XML 数据。

## 例子

展示如何为结构化文档标记的范围开始设置 XML 映射。

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// 构造一个包含文本的 XML 部件并将其添加到文档的 CustomXmlPart 集合中。
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// 创建一个结构化的文档标记，它将在文档中显示我们的 CustomXmlPart 的内容。
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// 如果我们为结构化文档标签设置映射，
// 它只会显示 XPath 指向的 CustomXmlPart 的一部分。
// 这个 XPath 将指向内容的第二个“<text>”第一个“<root>”的元素我们的 CustomXmlPart 的元素。
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### 也可以看看

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
