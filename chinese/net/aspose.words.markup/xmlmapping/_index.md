---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.XmlMapping 类，将结构化文档标签与 XML 元素无缝链接，增强文档的数据集成。
type: docs
weight: 4790
url: /zh/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

指定用于在 parent 结构化文档标记和存储在文档中的自定义 XML 数据部分中的 XML 元素之间建立映射的信息。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class XmlMapping
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | 返回父结构化文档标签映射到的自定义 XML 数据部分。 |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | 返回`真的`如果父结构化文档标签成功映射到 XML 数据。 |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | 返回 XML 命名空间前缀映射以评估[`XPath`](./xpath/). |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | 指定自定义 XML 数据部分的自定义 XML 数据标识符，该标识符应用于评估[`XPath`](./xpath/)表达式. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | 返回 XPath 表达式，该表达式用于查找映射到父结构化文档标签的自定义 XML 节点 。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | 删除父结构化文档到 XML 数据的映射。 |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | 设置父结构化文档标签和自定义 XML 数据部分的 XML 节点之间的映射。 |

## 例子

展示如何为自定义 XML 部分设置 XML 映射。

```csharp
Document doc = new Document();

// 构造一个包含文本的 XML 部分并将其添加到文档的 CustomXmlPart 集合中。
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// 创建一个结构化文档标签，它将显示我们的 CustomXmlPart 的内容。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// 为我们的结构化文档标签设置一个映射。此映射将指示
// 我们的结构化文档标签显示 XPath 指向的 XML 部分文本内容的一部分。
// 在这种情况下，它将是第一个“<root>”元素的第二个“<text>”元素的内容：“Text element #2”。
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// 将结构化文档标签添加到文档中以显示来自我们自定义部分的内容。
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
