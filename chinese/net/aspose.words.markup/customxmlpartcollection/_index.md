---
title: CustomXmlPartCollection Class
linktitle: CustomXmlPartCollection
articleTitle: CustomXmlPartCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Markup.CustomXmlPartCollection 班级. 表示自定义 XML 部件的集合这些项目是CustomXmlPart对象 在 C#.
type: docs
weight: 3930
url: /zh/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

表示自定义 XML 部件的集合。这些项目是[`CustomXmlPart`](../customxmlpart/)对象.

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | 获取或设置指定索引处的项目。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(*[CustomXmlPart](../customxmlpart/)*) | 将项目添加到集合中。 |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(*string, string*) | 使用指定的 XML 创建新的 XML 部分并将其添加到集合中。 |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | 从集合中删除所有元素。 |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | 制作此集合及其项目的深层副本。 |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(*string*) | 按标识符查找并返回自定义 XML 部分。 |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(*int*) | 删除指定索引处的项目。 |

## 评论

您通常不需要创建此类的实例。您可以通过以下方式访问存储在文档中的自定义 XML 数据 [`CustomXmlParts`](../../aspose.words/document/customxmlparts/)财产。

## 例子

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

* class [CustomXmlPart](../customxmlpart/)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
