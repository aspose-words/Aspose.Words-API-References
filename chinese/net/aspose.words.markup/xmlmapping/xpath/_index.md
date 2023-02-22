---
title: XmlMapping.XPath
second_title: Aspose.Words for .NET API 参考
description: XmlMapping 财产. 返回 XPath 表达式计算该表达式以找到映射到父结构化文档标记的自定义 XML 节点 
type: docs
weight: 50
url: /zh/net/aspose.words.markup/xmlmapping/xpath/
---
## XmlMapping.XPath property

返回 XPath 表达式，计算该表达式以找到映射到父结构化文档标记的自定义 XML 节点 。

```csharp
public string XPath { get; }
```

### 例子

展示如何为自定义 XML 部件设置 XML 映射。

```csharp
Document doc = new Document();

// 构造一个包含文本的 XML 部件并将其添加到文档的 CustomXmlPart 集合中。
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>", 
    Encoding.UTF8.GetString(xmlPart.Data));

// 创建一个结构化的文档标签，它将显示我们的 CustomXmlPart 的内容。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// 为我们的结构化文档标签设置一个映射。该映射将指示
// 我们的结构化文档标记，用于显示 XPath 指向的部分 XML 部分的文本内容。
// 在这种情况下，它将是第二个“<text>”的内容第一个“<root>”的元素元素：“文本元素#2”。
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// 将结构化文档标签添加到文档以显示来自我们自定义部分的内容。
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### 也可以看看

* class [XmlMapping](../)
* 命名空间 [Aspose.Words.Markup](../../xmlmapping/)
* 部件 [Aspose.Words](../../../)


