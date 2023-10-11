---
title: CustomPartCollection.Item
second_title: Aspose.Words for .NET API 参考
description: CustomPartCollection 财产. 获取或设置指定索引处的项目
type: docs
weight: 30
url: /zh/net/aspose.words.markup/custompartcollection/item/
---
## CustomPartCollection indexer

获取或设置指定索引处的项目。

```csharp
public CustomPart this[int index] { get; set; }
```

| 范围 | 描述 |
| --- | --- |
| index | 项目的从零开始的索引。 |

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

* class [CustomPart](../../custompart/)
* class [CustomPartCollection](../)
* 命名空间 [Aspose.Words.Markup](../../custompartcollection/)
* 部件 [Aspose.Words](../../../)


