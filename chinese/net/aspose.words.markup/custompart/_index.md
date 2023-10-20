---
title: CustomPart Class
linktitle: CustomPart
articleTitle: CustomPart
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Markup.CustomPart 班级. 表示自定义任意内容部分ISO/IEC 29500 标准未定义 在 C#.
type: docs
weight: 3900
url: /zh/net/aspose.words.markup/custompart/
---
## CustomPart class

表示自定义（任意内容）部分，ISO/IEC 29500 标准未定义。

要了解更多信息，请访问[结构化文档标签或内容控制](https://docs.aspose.com/words/net/working-with-content-control-sdt/)文档文章。

```csharp
public class CustomPart
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CustomPart](custompart/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | 指定此自定义部分的内容类型。 |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | 包含此自定义部件的数据。 |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | 如果此自定义部分存储在 OOXML 包内，则为 False。如果此自定义部件是外部目标，则为 True。 |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | 获取或设置该部分在 OOXML 包或目标 URL 中的绝对名称。 |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | 获取或设置从父部件到此自定义部件的关系类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | 制作对象的“足够深”的副本。 不重复字节[`Data`](./data/)值. |

## 评论

此类表示作为“未知关系”目标的 OOXML 部分。 ISO/IEC 29500 中未定义的所有关系都被视为“未知关系”。 Office Open XML 文档中允许未知关系，只要它们 符合关系标记指南。

Microsoft Word 在打开/保存周期期间保留自定义部分。一些附加信息可以在这里找到 http://blogs.msdn.com/dmahugh/archive/2006/11/25/任意-content-in-an-opc-package.aspx

Aspose.Words 还可以往返自定义部件，此外，还允许通过以下方式以编程方式访问 此类部件：`CustomPart`和[`CustomPartCollection`](../custompartcollection/)对象。

不要将自定义部件与自定义 XML 数据混淆。使用[`CustomXmlPart`](../customxmlpart/)如果您需要 来访问自定义 XML 数据。

## 例子

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

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
