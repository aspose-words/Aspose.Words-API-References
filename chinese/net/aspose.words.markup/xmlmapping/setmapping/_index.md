---
title: XmlMapping.SetMapping
linktitle: SetMapping
articleTitle: SetMapping
second_title: Aspose.Words for .NET
description: 了解 XmlMapping SetMapping 方法如何将父结构化文档连接到自定义 XML 节点，从而增强数据集成和管理。
type: docs
weight: 70
url: /zh/net/aspose.words.markup/xmlmapping/setmapping/
---
## XmlMapping.SetMapping method

设置父结构化文档标签和自定义 XML 数据部分的 XML 节点之间的映射。

```csharp
public bool SetMapping(CustomXmlPart customXmlPart, string xPath, string prefixMapping)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| customXmlPart | CustomXmlPart | 要映射到的自定义 XML 数据部分。 |
| xPath | String | 用于查找 XML 节点的 XPath 表达式。 |
| prefixMapping | String | XML 命名空间前缀映射来评估 XPath。 |

### 返回值

指示父结构化文档标签是否成功映射到 XML 节点的标志。

## 例子

展示如何使用自定义 XML 数据创建结构化文档标签。

```csharp
Document doc = new Document();

// 构建包含数据的 XML 部分并将其添加到文档的集合中。
// 如果我们在 Microsoft Word 中启用“开发人员”选项卡，
// 我们可以在“XML 映射窗格”中找到该集合中的元素，以及一些默认元素。
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// 下面是两种引用 XML 部分的方法。
// 1 - 通过自定义 XML 部分集合中的索引：
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - 按 GUID：
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// 添加 XML 模式关联。
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// 克隆一个部分，然后将其插入到集合中。
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// 遍历集合并打印每个部分的内容。
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// 使用“RemoveAt”方法通过索引删除克隆的部分。
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// 克隆 XML 部分集合，然后使用“Clear”方法一次性删除其所有元素。
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// 创建一个结构化文档标签，它将显示我们部分的内容并将其插入到文档正文中。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### 也可以看看

* class [CustomXmlPart](../../customxmlpart/)
* class [XmlMapping](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
