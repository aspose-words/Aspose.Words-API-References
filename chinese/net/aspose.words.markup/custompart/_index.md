---
title: Class CustomPart
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Markup.CustomPart 班级. 表示 ISO/IEC 29500 标准未定义的自定义任意内容部分
type: docs
weight: 3660
url: /zh/net/aspose.words.markup/custompart/
---
## CustomPart class

表示 ISO/IEC 29500 标准未定义的自定义（任意内容）部分。

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
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | 指定此自定义部件的内容类型。 |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | 包含此自定义零件的数据。 |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | `错误的`如果此自定义部件存储在 OOXML 包中。`真的`如果此自定义部件是外部目标。 |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | 获取或设置此部分在 OOXML 包或目标 URL 中的绝对名称。 |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | 获取或设置从父部件到此自定义部件的关系类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | 制作对象的“足够深”的副本。 不复制[`Data`](./data/)值. |

### 评论

此类表示作为“未知关系”目标的 OOXML 部分。 未在 ISO/IEC 29500 中定义的所有关系都被视为“未知关系”。 Office Open XML 文档中允许存在未知关系，前提是它们 符合关系标记指南。

Microsoft Word 在打开/保存周期中保留自定义部分。一些额外的信息可以在这里找到 http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words 还往返自定义部件，此外，允许通过编程访问 这样的部件`CustomPart`和[`CustomPartCollection`](../custompartcollection/)对象。

不要将自定义部件与自定义 XML 数据混淆。利用[`CustomXmlPart`](../customxmlpart/)如果您需要 来访问自定义 XML 数据。

### 例子

显示如何访问文档的任意自定义部件集合。

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

// 我们可以从这个集合中单独删除元素，也可以一次全部删除。
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)


