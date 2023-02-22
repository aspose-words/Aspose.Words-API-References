---
title: CustomXmlSchemaCollection.RemoveAt
second_title: Aspose.Words for .NET API 参考
description: CustomXmlSchemaCollection 方法. 删除指定索引处的值
type: docs
weight: 90
url: /zh/net/aspose.words.markup/customxmlschemacollection/removeat/
---
## CustomXmlSchemaCollection.RemoveAt method

删除指定索引处的值。

```csharp
public void RemoveAt(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 从零开始的索引。 |

### 例子

展示如何使用 XML 模式集合。

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// 添加一个 XML 模式关联。
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// 克隆自定义 XML 部分的 XML 模式关联集合，
// 然后将几个新模式添加到克隆中。
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// 枚举模式并打印每个元素。
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// 下面是从集合中删除模式的三种方法。
// 1 - 按索引删除模式：
schemas.RemoveAt(2);

// 2 - 按值删除模式：
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - 使用“Clear”方法一次清空集合。
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### 也可以看看

* class [CustomXmlSchemaCollection](../)
* 命名空间 [Aspose.Words.Markup](../../customxmlschemacollection/)
* 部件 [Aspose.Words](../../../)


