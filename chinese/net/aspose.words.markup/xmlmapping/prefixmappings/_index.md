---
title: XmlMapping.PrefixMappings
linktitle: PrefixMappings
articleTitle: PrefixMappings
second_title: Aspose.Words for .NET
description: 探索 XmlMapping PrefixMappings 属性，实现无缝的 XML 命名空间前缀映射和高效的 XPath 计算。立即增强您的 XML 处理能力！
type: docs
weight: 30
url: /zh/net/aspose.words.markup/xmlmapping/prefixmappings/
---
## XmlMapping.PrefixMappings property

返回 XML 命名空间前缀映射以评估[`XPath`](../xpath/).

```csharp
public string PrefixMappings { get; }
```

## 评论

指定一组前缀映射，当根据文档中的自定义 XML 数据部分评估 XPath 表达式时，应使用该前缀映射来解释 XPath 表达式。

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

* class [XmlMapping](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
