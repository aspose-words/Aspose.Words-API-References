---
title: CustomPart.Data
linktitle: Data
articleTitle: Data
second_title: Aspose.Words for .NET
description: 探索定制零件数据。获取定制零件的详细信息，提高项目的精度和效率。
type: docs
weight: 30
url: /zh/net/aspose.words.markup/custompart/data/
---
## CustomPart.Data property

包含此自定义部分的数据。

```csharp
public byte[] Data { get; set; }
```

## 评论

此属性仅适用于[`IsExternal`](../isexternal/)是`错误的`。

默认值为空字节数组。该值不能`无效的`。

## 例子

展示如何访问文档的任意自定义部分集合。

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

* class [CustomPart](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
