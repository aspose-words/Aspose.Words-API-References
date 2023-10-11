---
title: Class CustomPartCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Markup.CustomPartCollection 班级. 代表集合CustomPart对象.
type: docs
weight: 3910
url: /zh/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

代表集合[`CustomPart`](../custompart/)对象.

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class CustomPartCollection : IEnumerable<CustomPart>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CustomPartCollection](custompartcollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | 获取集合中包含的元素数量。 |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | 获取或设置指定索引处的项目。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(CustomPart) | 将项目添加到集合中。 |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | 从集合中删除所有元素。 |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | 制作此集合及其项目的深层副本。 |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | 返回一个枚举器对象，可用于迭代集合中的所有项目。 |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(int) | 删除指定索引处的项目。 |

### 评论

您通常不需要创建此类的实例。您可以通过以下方式访问与 OOXML 包相关的自定义部分 [`PackageCustomParts`](../../aspose.words/document/packagecustomparts/)财产。

### 例子

演示如何访问文档的任意自定义部件集合。

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// 克隆第二部分，然后将克隆添加到集合中。
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// 枚举集合并打印每个部分。
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

// 我们可以从该集合中单独删除元素，也可以一次性删除所有元素。
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### 也可以看看

* class [CustomPart](../custompart/)
* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)


