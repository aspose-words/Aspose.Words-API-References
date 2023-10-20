---
title: CustomXmlSchemaCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: 用于 .NET 的 Aspose.Words
description: CustomXmlSchemaCollection GetEnumerator 方法. 返回一个枚举器对象可用于迭代集合中的所有项目 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.markup/customxmlschemacollection/getenumerator/
---
## CustomXmlSchemaCollection.GetEnumerator method

返回一个枚举器对象，可用于迭代集合中的所有项目。

```csharp
public IEnumerator<string> GetEnumerator()
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

// 以下是从集合中删除模式的三种方法。
// 1 - 按索引删除模式：
schemas.RemoveAt(2);

// 2 - 按值删除模式：
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - 使用“Clear”方法立即清空集合。
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### 也可以看看

* class [CustomXmlSchemaCollection](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
