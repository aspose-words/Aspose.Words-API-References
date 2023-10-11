---
title: Class CustomXmlPart
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Markup.CustomXmlPart 班级. 表示自定义 XML 数据存储部分包内的自定义 XML 数据
type: docs
weight: 3920
url: /zh/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

表示自定义 XML 数据存储部分（包内的自定义 XML 数据）。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class CustomXmlPart
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | 获取或设置此自定义 XML 数据存储部分的 XML 内容。 |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | 指定循环冗余校验 (CRC) 校验和[`Data`](./data/)内容. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | 获取或设置在 OOXML 文档中标识此自定义 XML 部分的字符串。 |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | 指定与此自定义 XML 部分关联的 XML 架构集。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | 制作对象的“足够深”的副本。 不重复字节[`Data`](./data/)值. |

### 评论

DOCX 或 DOC 文档可以包含一个或多个自定义 XML 数据存储部分。 Aspose.Words 保留并 允许通过以下方式创建和提取自定义 XML 数据[`CustomXmlParts`](../../aspose.words/document/customxmlparts/)收藏。

### 例子

演示如何使用自定义 XML 数据创建结构化文档标签。

```csharp
Document doc = new Document();

// 构造一个包含数据的 XML 部分并将其添加到文档的集合中。
// 如果我们在 Microsoft Word 中启用“开发人员”选项卡，
// 我们可以在“XML 映射窗格”中找到该集合中的元素以及一些默认元素。
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// 下面是引用 XML 部分的两种方法。
// 1 - 通过自定义 XML 部件集合中的索引：
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - 通过 GUID：
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// 添加 XML 模式关联。
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// 克隆一部分，然后将其插入到集合中。
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

// 使用“RemoveAt”方法按索引删除克隆部分。
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// 克隆 XML 部件集合，然后使用“Clear”方法一次删除其所有元素。
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// 创建一个结构化文档标签，该标签将显示我们部分的内容并将其插入到文档正文中。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)


