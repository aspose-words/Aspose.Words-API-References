---
title: CustomXmlSchemaCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 探索 CustomXmlSchemaCollection Count 属性，轻松检索 XML 架构集合中的元素总数。优化您的数据管理！
type: docs
weight: 10
url: /zh/net/aspose.words.markup/customxmlschemacollection/count/
---
## CustomXmlSchemaCollection.Count property

获取集合中包含的元素数量。

```csharp
public int Count { get; }
```

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

* class [CustomXmlSchemaCollection](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
