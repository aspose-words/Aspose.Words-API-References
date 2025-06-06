---
title: CustomXmlSchemaCollection Class
linktitle: CustomXmlSchemaCollection
articleTitle: CustomXmlSchemaCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.CustomXmlSchemaCollection 类，用于管理链接到自定义 XML 部分的 XML 模式，增强文档的灵活性和控制力。
type: docs
weight: 4650
url: /zh/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

表示与自定义 XML 部分关联的 XML 架构的字符串集合。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | 获取或设置指定索引处的元素。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(*string*) | 将项目添加到集合。 |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | 从集合中删除所有元素。 |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | 对此对象进行深度克隆。 |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(*string*) | 返回集合中指定值的从零开始的索引。 |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(*string*) | 从集合中删除指定的值。 |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(*int*) | 删除指定索引处的值。 |

## 评论

您无需创建此类的实例。您可以通过以下方式访问自定义 XML part 的 XML 架构集合：[`Schemas`](../customxmlpart/schemas/)财产。

## 例子

展示如何使用 XML 架构集合。

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// 添加 XML 模式关联。
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// 克隆自定义 XML 部分的 XML 架构关联集合，
// 然后向克隆添加几个新模式。
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType”);

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType");

// 枚举模式并打印每个元素。
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// 以下是从集合中删除模式的三种方法。
// 1 - 通过索引删除模式：
schemas.RemoveAt(2);

// 2 - 通过值删除架构：
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - 使用“Clear”方法立即清空集合。
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
